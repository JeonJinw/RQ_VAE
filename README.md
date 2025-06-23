# 2025-01 생성형 모델
## Autoregressive Image Generation using Residual Quantization (CVPR 2022)
#### 환경 구축 방법 (Requirements)
- `Python 3.7.12 / torch==1.9.0+cu111 / torchvision==0.10.0+cu111 / torchaudio==0.9.0`
`pip install -r requirements.txt`
#### 사전 학습 모델 다운로드
다음 링크를 통해 FFHQ data set을 사용하여 사전 학습 완료된 RQ-VAE, RQ-Transformer 다운로드 (tar.gz).

- [FFHQ pretrained model link](https://twg.kakaocdn.net/brainrepo/models/RQVAE/d47570aeff6ba300735606a806f54663/ffhq.tar.gz)

다운로드 된 파일 압축 해제 후 다음 디렉토리에 각각 저장

- RQ-VAE 모델 파라미터: config/ffhq/stage1/
- RQ-Transformer 모델 파라미터: config/ffhq/stage2/
#### 특징 벡터 통계 다운로드
다음 링크르 통해 데이터 셋의 특징 벡터 통계 다운로드

- [Feature vector statistics](https://twg.kakaocdn.net/brainrepo/etc/RQVAE/8b325b628f49bf60a3094fcf9419398c/fid_stats.tar.gz)

다운로드된 파일 압축 해제 후 다음 디렉토리에 저장 : assets/

#### 결과 디렉토리 생성
추론 결과를 저장할 result 디렉토리 생성
#### 실행
`python main_sampling_fid.py -v .\configs\ffhq\stage1\model.pt -a .\configs\ffhq\stage2\model.pt --save-dir .\results\`


