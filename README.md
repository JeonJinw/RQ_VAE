# 2025-01 생성형 모델
## Autoregressive Image Generation using Residual Quantization (CVPR 2022)
#### 환경 구축 방법 (Requirements)
`pip install -r requirements.txt`
#### 사전 준비
1. FFHQ data set을 사용하여 사전 학습 완료된 RQ-VAE, RQ-Transformer 다운로드
2. RQ-VAE 모델 파라미터 압축 해제 후 다음 디렉토리에 저장 : config/ffhq/stage1/
3. RQ-Transformer 모델 파라미터 압축 해제 후 다음 디렉토리에 저장 : config/ffhq/stage2/
4. 데이터 셋의 특징 벡터 통계 다운로드 및 압축 해제 후 다음 디렉토리에 저장 : assets/
5. 추론 결과를 저장할 result 디렉토리 생성
#### 실행
`python main_sampling_fid.py -v .\configs\ffhq\stage1\model.pt -a .\configs\ffhq\stage2\model.pt --save-dir .\results\`


