# CPR-PAD 펌웨어 배포

CREDO G_PAD(CPR-PAD) 보드의 펌웨어(OTA DFU zip)를 올려 두는 곳입니다.
안드로이드 **CPR-PAD 업데이트** 앱이 [Releases](../../releases) 목록을 읽어 버전을 고르고, 받은 파일로 주변 보드를 한꺼번에 업데이트합니다.

- 각 릴리스에는 `gpad_fw_v<버전>.zip` 하나가 있습니다 (nrfutil 앱 단독 패키지 + `credo.sig` 서명).
- 앱은 서명이 맞지 않는 파일은 쓰지 않습니다.
- 보드는 지금보다 낮은 DFU 카운터의 펌웨어를 거부합니다 (다운그레이드 불가).
- 올리는 방법: 소스 저장소의 `python fw_publish.py publish <버전>` (서명 키가 있는 PC 에서만).
