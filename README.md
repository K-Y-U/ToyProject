# Fashion_MNIST 실험
기본 Fashion_MNSIT 분류 코드를 통해 정확도는 높게 나오지만 그래프를 통해 overfitting 유무를 확인을 하고 overfitting을 해결하기 위해 drop out 기법을 추가했습니다. 처음에는 overfitting을 해결 할 수 있다 생각하고 실행을 했지만 여전히 overfitting을 잡지를 못했습니다. 처음 시도한 방법은 정말 간단한 epoch를 조정해 봤습니다. 결과는 똑같이 overfitting을 확인 했습니다. 
여러번 시도 끝에 -> epoch = 20 / nn.Dropout(p=0.5)로 설정 했을 때 overfitting을 해결했습니다.
