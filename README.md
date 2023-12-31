# Fashion_MNIST 실험
기본 Fashion_MNSIT 분류 코드를 통해 정확도를 더 높게 잡는 실험으로 시작했으며 overfitting 해결하기 위한 실험을 해봤습니다.
그래프를 통해 얼만큼 loss를 최소화 했는지 확인했습니다.
그래프에서 overfitting를 확인하고 일어나는 이유를 생각했습니다.
첫 번째 모델의 복잡도를 생각했습니다.
이유는 정확도는 높지만 overfitting 일어났기 때문이라고 생각했습니다. 
결국 모델이 너무 복잡하여 해결하기 위해 Regularization에서 Drop out 기법을 사용했습니다.

Drop out 기법을 사용한 이유는 모델의 복잡도이기 때문입니다.
일반 신경망에서 모든 뉴런을 사용으로 인해 복잡도가 높은 반면 학습 과정에서 무작위로 몇개의 뉴런을 제외하는 Drop out 기법이기 때문입니다.

처음에는 overfitting을 해결 할 수 있다 생각하고 실행을 했지만 여전히 overfitting을 잡지를 못했습니다. 처음 시도한 방법은 정말 간단한 epoch를 조정해 봤습니다. 결과는 똑같이 overfitting을 확인 했습니다. 
여러번 시도 끝에 -> epoch = 20 / nn.Dropout(p=0.5)로 설정 했을 때 overfitting을 해결했습니다.

여러번 시도 끝에 overfitting을 해결 후 해결 한 이유를 코드를 통해 공부를 하고 있지만 명확한 답을 찾지 못했습니다. 공부를 통해 overfitting을 해결 하기 위한 여러 방법이 있지만 Drop out기법이 제일 이번 코드 실험에 적합하다고 생각했습니다.
