## Multidimensional Uncertainty-Aware Evidential Neural Networks



### What is new in the work?

- They proposed a novel uncertainty-aware evidential NN called WGAN-ENN for solving an OOD detection problem.<br>
    
- They combined Wasserstein Generative Adversarial Network (WGAN) with ENNs to jointly train model.


* ### Why is the work important?
    Tradition ENN has been proposed to explicitly model the uncertainty of class probabilities.

    But, it is trained as **Black box** without considering different types of uncertainty in data and it often results in overconfidence with OOD tests.

* ### What is the literature gap?
    Tradition ENN has been proposed to explicitly model the uncertainty of class probabilities.

    But, it is trained as **Black box** without considering different types of uncertainty in data and it often results in overconfidence with OOD tests, distingushing boundary samples.

    Sensoy의 ENN은 예측 확률의 엔트로피만으로 불확실성을 측정했기 때문에, 불확실성의 원인에 대한 구분이 불가능합니다.
    OOD 탐지에서 과신(overconfidence) 문제가 발생하며, 경계 샘플과 OOD 샘플을 구분하는 데 한계가 있습니다.
    엔트로피(entropy)는 단순히 확률 분포의 퍼짐 정도만 측정합니다.

    하지만 vacuity와 dissonance는 서로 다른 원인에서 비롯된 불확실성입니다:

    vacuity는 증거 부족 → OOD 샘플에서 자주 발생
    vacuity는 증거 총량이 적을 때 높게 측정됨

    OOD 샘플은 학습 데이터에서 본 적 없는 분포 → evidence 자체가 거의 없음

    따라서 vacuity는 OOD 탐지에 효과적

    dissonance는 증거 충돌 → 경계 샘플에서 자주 발생

    따라서 엔트로피만으로는 이 둘을 구분할 수 없습니다. 기존 EDL에서 정의한 uncertainty가 entropy(확률 분포의 퍼짐 정도)로 정의된거라서 더 디테일하고 중요한 uncertainty 정도인 vacuity, dissonance 같은 척도들을 감지를 못 합니다.

    To solve this, regularization methods have been proposed to hand-pick-auxiliary OOD samples to train model. But this requires a lot of OOD samples.

(4) how is the gap filled

(5) what is achieved with the new method

(6) what data are used

(7) what are the limitations.
