아래는 YHHighschool 프로젝트의 README.md 파일에 추가할 수 있는 설명과 실행 방법입니다.

YHHighschool

이 프로젝트는 Python과 OpenCV를 활용하여 얼굴 인식 및 스티커 적용 기능을 구현한 애플리케이션입니다.

주요 기능
	•	얼굴 인식: Dlib 라이브러리를 사용하여 이미지에서 얼굴을 감지합니다.
	•	랜드마크 검출: 얼굴의 주요 특징점을 찾아냅니다.
	•	스티커 적용: 검출된 랜드마크를 기반으로 특정 위치에 스티커(예: 왕관)를 적용합니다.

설치 방법
	1.	필수 라이브러리 설치: 다음의 Python 라이브러리가 필요합니다.
	•	opencv-python
	•	dlib
	•	numpy
	•	matplotlib
라이브러리는 다음 명령어로 설치할 수 있습니다:

pip install opencv-python dlib numpy matplotlib


	2.	Dlib 모델 다운로드: 얼굴 랜드마크 검출을 위해 Dlib의 사전 학습된 모델이 필요합니다. 다음 명령어로 모델을 다운로드하고 압축을 해제한 후, 프로젝트 디렉토리의 models 폴더에 저장하세요:

wget http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2
bzip2 -d shape_predictor_68_face_landmarks.dat.bz2
mkdir -p models
mv shape_predictor_68_face_landmarks.dat models/



실행 방법
	1.	이미지 준비: 얼굴이 포함된 이미지를 프로젝트 디렉토리에 준비합니다.
	2.	스티커 이미지 준비: 적용할 스티커 이미지를 stickers 폴더에 저장합니다. 스티커 이미지는 투명 배경을 가진 PNG 형식이어야 합니다.
	3.	스크립트 실행: 다음 명령어로 스크립트를 실행합니다:

python E3_camera_sticker_app.py --image_path <이미지_경로> --sticker_path <스티커_경로>

예시:

python E3_camera_sticker_app.py --image_path ./images/face.jpg --sticker_path ./stickers/crown.png


	4.	결과 확인: 스티커가 적용된 결과 이미지는 output 폴더에 저장됩니다.

파일 구조

YHHighschool/
├── E3_camera_sticker_app.py       # 메인 스크립트
└── README.md                     # 프로젝트 설명서

참고 사항
	•	입력 이미지의 얼굴이 명확하게 보여야 정확한 인식이 가능합니다.
	•	스티커 이미지는 투명 배경을 가진 PNG 형식을 사용하는 것이 좋습니다.
