유전 알고리즘은 전역 최적화 기법입니다.

최적화 알고리즘이란 목표로 하는 최적화 값(일반적으로 MAX,MIN)을 각 탐색 범위 내에서 조절함으로써 주어진 비용함수의 값을 최소화 또는 최대화하는 해를 찾아내는 방법을 지칭합니다.

그중 전역 최적화 기법은 다소 시간이 조금 걸리지만 전체 탐색영역에서 가장 좋은 해를 찾는 것을 
목표로 합니다.

유전자 알고리즘에서는 풀고자 하는 문제에 대한 가능한 해들을 정해진 형태의 자료구조로 표현한 이후 이들을 점차 변형함으로써 더 좋은 해들을 만들어 나가는
과정을 거칩니다.

배열 chromosome은 염색체입니다. 유전물질 gene을 담고 있는 하나의 집합, 배열이며 7개의 random한 값을 갖는 gene을 담는 10개의 
chromosome을 갖는 5개의 개체를 생성하였습니다.

offspring은 특정 시간 t에 존재했던 염색체들로부터 생성된 염색체를 t에 존재했던 염색체들의 자손 
이라고 합니다. 이전의 세대와 비슷한 유전정보를 갖는 특징이 있습니다.

fitness 어떤 염색체가 갖고 있는 고유한 적합도 입니다. 해당 문제에 염색체가 표현하는 해가
얼마나 적합한지를 표현합니다.

1.초기에는 이전 염색체가 존재하지 않기 때문에 초기 염색체를 생성하는 연산을 임의의 값으로 정하였습니다.

2.적합도를 기준으로 염색체를 선택할때 다양성을 위해 룰렛 휠 방법을 사용합니다.

적합도가 더 큰 염색체가 룰렛 휠의 큰 비율을 차지하게 되면서 선택될 확률을 높입니다.
확률만 높일 뿐 단순하게 큰 적합도를 가지고 있는 염색체들을 선택하는 방법과는 다르게 다양성을 유지
할 수 있습니다.

3.룰렛 휠 방식으로 선택된 부모 염색체들로부터 자손을 생성합니다.
crossover이라는 연산을 이용할 것 인데 이는 부모 염색체에서 분할지점을 임의적으로 선택해
그 지점을 기준으로 parent1 과 parent2의 배열을 섞습니다.

4.유전 알고리즘에서는 지역 최적점에 빠지는 문제를 해결하기 위해 새롭게 생성된 염색체에
확률적으로 돌연변이가 발생하도록 합니다. 아주 낮은 확률로 돌연변이가 발생하도록 설정하며,
돌연변이 연산에는 다양한 방법을 접목시킬수 있습니다.
대표적으로는 reverse 나 exchage의 방식으로 예로 들수있는데, reverse의 경우 chromosome배열의
값중 하나를 임의로 선택하여 0이면 1로 1이면 0으로 reverse합니다.

exchange 방식의 경우 배열 중 두 임의의 자리값을 서로 교환합니다.
























