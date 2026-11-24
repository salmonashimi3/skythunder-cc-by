# Sky Thunder (스카이 썬더)

브라우저에서 하는 제트기 공중전 게임입니다. F-5E로 시작해 판을 거듭하며 격납고 레벨을 올리고, 코인을 모아 F-14D Super Tomcat까지 14대를 해금합니다. 개발자 패스 코드를 입력하면 모든 기체가 한 번에 해금됩니다.

## 플레이

GitHub Pages로 배포하면 `https://<아이디>.github.io/<저장소 이름>/` 주소에서 바로 할 수 있습니다.

## 게임 내용

- 처음 실행하면 튜토리얼 (선회 · 스로틀 · 시점 · 기관포 · 락온 미사일 · 플레어)
- 5대5 팀 데스매치: 먼저 20킬 또는 7분 뒤 점수가 높은 팀 승리
- 10판마다 격납고 레벨 +1 → 다음 기체 구매 가능
- 기체마다 다른 체력 · 속도 · 기동성 · 기관포 위치 · 미사일
- 도색 7종, 업그레이드 4종 (엔진 · 장갑 · 기관포 · 미사일, 각 5단계)

## 조작

| 동작 | 키 |
|---|---|
| 조준 / 선회 | 마우스 |
| 기관포 | 좌클릭 |
| 미사일 (락온 필요) | 우클릭 · Space |
| 미사일 종류 | 1 · 2 |
| 스로틀 | Shift · X · 휠 |
| 시점 전환 | V |
| 자유 시점 | C 누르기 |
| 플레어 | F |
| 수동 조종 | W S A D Q E · 방향키 |
| 음소거 · 일시정지 | M · Esc |

## 파일

- `index.html` 게임 본체 (three.js는 CDN에서 불러옵니다)
- `planes.js` 기체 목록과 성능표
- `models/` 기체 3D 모델 (glb)

`index.html`을 더블클릭으로 열면 모델을 불러오지 못합니다. GitHub Pages 같은 웹 서버에 올려서 여세요.

진행 상황(코인, 해금)은 각자 브라우저에 저장됩니다.

## 3D 모델 출처 · 라이선스

기체 모델은 모두 Sketchfab에서 받은 **CC BY 4.0** 모델입니다. 상업적 이용은 허용되고, 출처 표시 조건을 따릅니다 (https://creativecommons.org/licenses/by/4.0/).

| 게임 속 기체 | 파일 | 원본 모델 · 제작자 | 원본 링크 | 변경 사항 |
|---|---|---|---|---|
| F-5E Tiger II | `models/f5.glb` | F5 · manilov.ap | https://sketchfab.com/3d-models/f5-8089d66a8a8748b2a4b049b3c06f6a02 | 없음 |
| A-10C Thunderbolt II | `models/a10.part0`~`part3` | A-10 ThunderBolt II · KOG_THORNS | https://sketchfab.com/3d-models/a-10-thunderbolt-ii-623514b5f1f9483a9bbee7f25da77468 | 텍스처를 1024px WebP로 줄여 최적화 · 파일 하나가 25MB라 4개 조각(8MB 단위)으로 나눠 저장 (로더가 합쳐서 읽음) |
| F-117A Nighthawk | `models/f117.glb` | F117 Nighthawk · agreene | https://sketchfab.com/3d-models/f117-nighthawk-f97abc471f094013a77a88a1191f890e | 없음 |
| F-4E Phantom II | `models/f4.glb` | F4 phantom ii · dragon22blockbench | https://sketchfab.com/3d-models/f4-phantom-ii-97cbebec399543bbafa289f22aea0806 | 없음 |
| F-15C Eagle | `models/f15.glb` | F 15 C (Pixy) · Uxman | https://sketchfab.com/3d-models/f-15-c-pixy-b31c02e554f74ab68aa8610334c744c3 | 없음 |
| F/A-18F Super Hornet | `models/f18.glb` | Boeing F/A-18E/F Super Hornet · andertan | https://sketchfab.com/3d-models/boeing-fa-18ef-super-hornet-f71e9fea01e24fea9b1b380161d21d38 | 재질을 metallic-roughness로 변환 |
| Su-27 Flanker-B | `models/su27.glb` | Ukrainian Su-27B · 42manako | https://sketchfab.com/3d-models/ukrainian-su-27b-a1fa957a39bb4f3db8bb669c2dd6afdb | 없음 |
| Su-30 Flanker-C | `models/su30.glb` | Sukhoi Su-30 Flanker C · andertan | https://sketchfab.com/3d-models/sukhoi-su-30-flanker-c-92ca062c90fd45ffb6ce8144dc46004a | 없음 |
| Su-34 Fullback | `models/su34.glb` | Su34 · manilov.ap | https://sketchfab.com/3d-models/su34-1c94f436be51453fa598e9eab50eb0a7 | 없음 |
| Su-35 Flanker-E | `models/su35.glb` | Sukhoi Su-35 Flanker-E · andertan | https://sketchfab.com/3d-models/sukhoi-su-35-flanker-e-35-c98cf9b3b3e04017a04732798a31888a | 없음 |
| Su-57 Felon | `models/su57.glb` | Sukhoi Su-57 Felon · andertan | https://sketchfab.com/3d-models/sukhoi-su-57-felon-09d546b4355c4fa6882ca46e05069bee | 없음 |
| F-22A Raptor | `models/f22.glb` | F22 Raptor · Astral (Astral_27) | https://sketchfab.com/3d-models/f22-raptor-f7e8ca7bd6ee404a9653aa3af0c25b81 | 없음 |
| F-35A Lightning II | `models/f35.glb` | Lockheed Martin F35 Lightning II · andertan | https://sketchfab.com/3d-models/lockheed-martin-f35-lightning-ii-db911de503c74285a8d506951df786d6 | 없음 |
| F-14D Super Tomcat | `models/f14.part0`~`part2` | Grumman F-14D "Super Tomcat" · KOG_THORNS | https://sketchfab.com/3d-models/grumman-f-14d-super-tomcat-74be89a104a34caabacb25a705708097 | 없음 (3개 파일로 나눠 저장) |
| KC-46A Pegasus (급유기) | `models/kc46.glb` | Boeing KC-46A Pegasus · Muhamad Mirza Arrafi | https://sketchfab.com/3d-models/boeing-kc-46a-pegasus-e6520680689c47f58e1c742b3bb11150 | 없음 |

모델 파일 안에도 `asset.extras`에 제작자와 라이선스가 들어 있습니다.
