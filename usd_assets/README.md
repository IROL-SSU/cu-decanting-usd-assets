# 디캔팅 제품 USD 에셋

Isaac Sim 5.1에서 사용할 수 있도록 제작한 치수 기반 프록시 에셋입니다.

## 빠른 확인

Isaac Sim에서 `preview_scene.usd`를 열면 모든 외곽 상자와 내부 제품을 한 장면에서 확인할 수 있습니다. 장면에는 GPU PhysX Scene, 바닥 충돌체, 조명, 카메라가 포함되어 있습니다. Play를 누르면 rigid 및 deformable 낙하와 충돌을 바로 확인할 수 있습니다.

USD 파일들은 상대 경로로 참조되므로 `usd_assets` 폴더 구조를 유지해야 합니다.

## 파일 구성

| 제품 | 외곽 상자 | 내부 제품 |
|---|---|---|
| 아이셔-청사과맛 | `aishyeo_green_apple/outer_box.usd` | `aishyeo_green_apple/inner_box_rigid.usd` |
| 코코망고알맹이 | `cocomango_gummy/outer_box.usd` | `cocomango_gummy/inner_box_rigid.usd` |
| 국수소면 | `somyeon_noodles/outer_box.usd` | `product_rigid.usd`, `product_deformable.usd` |
| 프루팁스 | `frutips/outer_box.usd` | `frutips/inner_box_rigid.usd` |
| 양반 참기름김 | `yangban_sesame_oil_seaweed/outer_box.usd` | `product_rigid.usd`, `product_deformable.usd` |
| 닥터유 단백질바 | `dr_you_protein_bar/outer_box.usd` | `product_rigid.usd` |
| 올뉴 비틀즈 | `all_new_beetles/outer_box.usd` | `product_rigid.usd` |
| 캇예스 베러버니사워 | `katjes_better_bunny_sour/outer_box.usd` | `product_rigid.usd`, `product_deformable.usd` |
| 자일라 페퍼민트껌 | `xyla_peppermint_gum/outer_box.usd` | `product_rigid.usd` |
| 구운쥐치포 | `grilled_filefish/outer_box.usd` | `product_rigid.usd`, `product_deformable.usd` |
| 맥반석 왕오징어구이 | `charcoal_grilled_squid/outer_box.usd` | `product_rigid.usd`, `product_deformable.usd` |
| 와사비맛땅콩 | `wasabi_peanuts/outer_box.usd` | `product_rigid.usd`, `product_deformable.usd` |
| 박카스 사워젤리 | `bacchus_sour_jelly/outer_box.usd` | `product_rigid.usd` |
| 비달 사우어레인보우믹스 | `vidal_sour_rainbow_mix/outer_box.usd` | `product_rigid.usd`, `product_deformable.usd` |
| 더 자일리톨 용기껌 | `the_xylitol_container_gum/outer_box.usd` | `inner_box_rigid.usd`, `product_rigid.usd` |
| 맛밤 | `matbam/outer_box.usd` | `product_rigid.usd`, `product_deformable.usd` |
| 짱매워요 엽떡매운맛 | `jjangmaewoyo_yeopdduk/outer_box.usd` | `product_rigid.usd` |
| 츄파춥스 사워바이츠 | `chupachups_sour_bites/outer_box.usd` | `product_rigid.usd` |
| 콜라향 츄잉캔디 | `cola_chewing_candy/outer_box.usd` | `product_rigid.usd` |
| 츄파춥스 플러피판다 | `chupachups_fluffy_panda/outer_box.usd` | `product_rigid.usd` |

## 모델링 기준

- 내부 단위: metre (`metersPerUnit = 1`)
- 입력 치수 단위: cm
- 치수 축 순서: 입력값 그대로 `X × Y × Z`
- Up axis: Z
- 피벗: 바닥면 중앙
- 외곽 상자: 디캔팅용 상단 개방형 5면 상자
- 외곽 상자 벽 두께: 4 mm 가정
- rigid 에셋: rigid body, compound/convex collision, CCD 적용
- 모양 변형 제품: 닫힌 pillow 형상의 rigid 및 PhysX volumetric deformable body를 모두 제공
- 원통형 제품: 지름과 높이에 맞춘 Z축 원통 및 원통 충돌체
- 더 자일리톨 용기껌: 외곽 상자, 안 상자, 낱개 원통 용기를 별도 USD로 제공

## 물성 가정

정확한 실측 무게와 재질 물성이 제공되지 않은 값은 초기 실험용 가정값입니다.

- 아이셔 내부 상자: 0.60 kg
- 코코망고 내부 상자: 0.76 kg
- 프루팁스 내부 상자: 0.70 kg
- 소면 낱개: 제품명에 근거해 0.90 kg
- 모든 deformable 초기 Young's modulus: 250,000 Pa
- 모든 deformable 초기 Poisson's ratio: 0.35
- 소면 질량: 0.90 kg, 밀도 약 666.67 kg/m³
- 그 외 질량과 밀도: 제품명에 중량이 있는 경우 이를 사용하고, 나머지는 초기 실험용 추정값 사용

실측값을 확보하면 질량, 마찰계수, 반발계수 및 deformable 재질값을 교체해야 합니다. 각 값은 USD의 `Physics` 및 `userProperties`에서 확인할 수 있습니다.

## 검증

`validation_report.json`에 결과가 저장되어 있습니다.

- 제품 20종, 개별 USD 49개 로드 성공
- 입력 치수와 생성 형상 치수 일치
- 모든 rigid body 및 collider 스키마 확인
- deformable body 및 collision 스키마 확인
- Isaac Sim 5.1에서 240-step rigid/deformable 낙하 테스트 통과

## 재생성 및 검증

저장소 루트에서 다음과 같이 실행합니다.

```bash
conda run --no-capture-output -n env_isaaclab python tools/generate_usd_assets.py
conda run --no-capture-output -n env_isaaclab python tools/validate_usd_assets.py
```

소면 deformable 에셋은 현재 설치된 Isaac Sim 5.1에서 검증된 PhysX deformable API를 사용합니다.
