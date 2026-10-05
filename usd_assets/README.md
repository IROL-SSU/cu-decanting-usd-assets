# 디캔팅 제품 USD 에셋

Isaac Sim 5.1에서 사용할 수 있도록 제작한 치수 및 제품 사진 기반 에셋입니다.

## 빠른 확인

Isaac Sim에서 `preview_scene.usd`를 열면 모든 외곽 상자와 내부 제품을 한 장면에서 확인할 수 있습니다. 장면에는 GPU PhysX Scene, 바닥 충돌체, 조명, 카메라가 포함되어 있습니다. Play를 누르면 rigid 및 deformable 낙하와 충돌을 바로 확인할 수 있습니다.

USD 파일들은 상대 경로로 참조되므로 `usd_assets` 폴더 구조를 유지해야 합니다.

각 제품 폴더의 `textures/product_label.jpg`는 제공된 실물 사진에서 포장 영역을 추출한 텍스처입니다. 박스 제품은 주요 노출면에, 파우치 제품은 변형 가능한 표면 전체에 UV로 연결되어 있습니다.

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

## 크기 비교표

> 외곽 박스와 제품 크기는 모두 X × Y × Z 순서이며 단위는 cm입니다.

| No. | 제품명 | 외곽 박스 크기 (cm) | 제품 크기 (cm) |
|---|---|---|---|
| 01 | 아이셔-청사과맛 | 32.5 × 28 × 13.5 | 26 × 8 × 11.5 |
| 02 | 코코망고알맹이 | 43 × 21.3 × 15 | 20 × 10.8 × 14.1 |
| 03 | 국수소면 | 37.5 × 24.5 × 20.3 | 12.5 × 27 × 4 |
| 04 | 프루팁스 | 48.7 × 25 × 15.5 | 8 × 24 × 14.5 |
| 05 | 양반 참기름김 | 53 × 32.5 × 27.3 | 18.5 × 10 × 6.5 |
| 06 | 닥터유 단백질바 | 34 × 21.5 × 14 | 16.7 × 20.2 × 6.3 |
| 07 | 올뉴 비틀즈 | 31.6 × 23 × 25.8 | 15 × 21 × 8 |
| 08 | 캇예스 베러버니사워 | 38.5 × 19.5 × 14.5 | 11.5 × 15 × 1.5 |
| 09 | 자일라 페퍼민트껌 | 39.2 × 25.5 × 18.7 | 9.6 × 24.5 × 4.3 |
| 10 | 구운쥐치포 | 52 × 36 × 27.2 | 25.1 × 17 × 0.2 |
| 11 | 맥반석 왕오징어구이 | 52 × 36 × 27.2 | 25.1 × 17 × 0.2 |
| 12 | 와사비맛땅콩 | 28.5 × 22.5 × 19 | 14 × 12.3 × 4 |
| 13 | 박카스 사워젤리 | 49.7 × 26.5 × 17 | 24.5 × 9.5 × 15.5 |
| 14 | 비달 사우어레인보우믹스 | 26 × 15.5 × 15.2 | 12.5 × 16.5 × 2 |
| 15 | 더 자일리톨 용기껌 | 31 × 23 × 20.7 | 7 × 7 × 9.3 |
| 16 | 맛밤 | 31.3 × 21.7 × 21 | 18.5 × 6.5 × 2.5 |
| 17 | 짱매워요 엽떡매운맛 | 47 × 24.2 × 17 | 22.1 × 11.5 × 15 |
| 18 | 츄파춥스 사워바이츠 | 33.7 × 27.5 × 33 | 12.5 × 7.6 × 15 |
| 19 | 콜라향 츄잉캔디 | 35 × 35 × 21.2 | 11.5 × 11.5 × 19.9 |
| 20 | 츄파춥스 플러피판다 | 33.7 × 27.5 × 33 | 12.5 × 7.6 × 15 |

## 모델링 기준

- 내부 단위: metre (`metersPerUnit = 1`)
- 입력 치수 단위: cm
- 치수 축 순서: 입력값 그대로 `X × Y × Z`
- Up axis: Z
- 피벗: 바닥면 중앙
- 외곽 상자: 디캔팅용 상단 개방형 5면 상자
- 외곽 상자 벽 두께: 4 mm 가정
- rigid 에셋: rigid body, compound/convex collision, CCD 적용
- 모양 변형 제품: 사진 텍스처를 적용한 닫힌 pillow 형상의 rigid 및 PhysX volumetric deformable body 제공
- 프루팁스: 투명 포장 외피 안에 2 × 6 배열의 컵과 뚜껑을 모델링
- 콜라향 츄잉캔디: 투명 원통, 빨간 뚜껑, 라벨 밴드와 내부 캔디 형상 모델링
- 더 자일리톨 용기껌: 외곽 상자, 안 상자와 녹색/흰색 낱개 디스펜서 용기를 별도 제공
- 사진에 없는 외곽 운송 상자는 기존 상단 개방형 골판지 구조 유지

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
python tools/prepare_product_textures.py --source-dir /path/to/reference_photos
conda run --no-capture-output -n env_isaaclab python tools/generate_usd_assets.py
conda run --no-capture-output -n env_isaaclab python tools/validate_usd_assets.py
conda run --no-capture-output -n env_isaaclab python tools/render_asset_preview.py
```

텍스처 JPG는 저장소에 포함되어 있으므로 일반 사용자는 `prepare_product_textures.py`를 다시 실행할 필요가 없습니다. 이 명령은 원본 사진으로 텍스처를 다시 추출할 때만 사용합니다.

소면 deformable 에셋은 현재 설치된 Isaac Sim 5.1에서 검증된 PhysX deformable API를 사용합니다.
