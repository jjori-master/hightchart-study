### Highchart의 Line Chart  제대로 한번 알아보기

> 학습목표
>
> - Highchart의  LineChart의 기본을 그려본다.
> - 중요한 옵션정보가 무엇이고 어떻게 조작하는지 알아본다



#### 1. 기본 사용법

[Basic Line chart Demo](<https://jsfiddle.net/gh/get/library/pure/highcharts/highcharts/tree/master/samples/highcharts/demo/line-basic/>)

[api highcharts](<https://api.highcharts.com/highcharts>)

HightChart 주요 Options

- [***yAxis***](<https://api.highcharts.com/highcharts/yAxis>)

  > axis는 중심선이라는 뜻을 가짐, 
  >
  > ```
  > The Y axis or value axis. Normally this is the vertical axis, though if the chart is inverted this is the horizontal axis. In case of multiple axes, the yAxis node is an array of configuration objects.
  > 
  > Y 축 또는 값 축입니다. 일반적으로 이것은 세로 축이지만, 차트가 반전 된 경우 가로 축입니다. 다중 축의 경우 yAxis 노드는 구성 객체의 배열입니다.
  > 
  > 한글로 봐도 뭔지 잘 모르겠다...
  > ```
  >
  
- Y축 즉 세로축의 설정을 하는데 우선 [Basic Line chart Demo](<https://jsfiddle.net/gh/get/library/pure/highcharts/highcharts/tree/master/samples/highcharts/demo/line-basic/>) 에 나온 속성만 조사
  
    - ***yAxis.title***
  
      > The axis title, showing next to the axis line.
      > 축 제목 옆에 축 선 옆에 표시됩니다.
  
      - **yAxis.title.text **
  
        > The actual text of the axis title. Horizontal texts can contain HTML, but rotated texts are painted using vector techniques and must be clean text. The Y axis title is disabled by setting the text option to undefined.
        >
        > 축 제목의 실제 텍스트입니다. 수평 텍스트에는 HTML이 포함될 수 있지만 회전 텍스트는 벡터 기술을 사용하여 그려지며 텍스트는 깨끗해야합니다. 텍스트 옵션을 undefined로 설정하면 Y 축 제목을 사용할 수 없습니다.
  
        - x 축만 html을 사용하고 수직축은 사용할수 없다고 하는데 근데 html 적용되는디
          우선 이정도만 알아두자
  
- ***legend***

  > The legend is a box containing a symbol and name for each series item or point item in the chart. Each series (or points in case of pie charts) is represented by a symbol and its name in the legend.
  >
  > 범례는 차트의 각각에 대한 기호 및 이름을 포함하는 상자입니다. 각 시리즈 (또는 원형 차트의 경우 점)는 범례에 기호와 이름으로 표시됩니다.

  - 한마디로 범례를 설정하는 부분,  데모에서는 레이아웃, 좌우 어디에 배치할 것인지
    상중하 정렬은 어떻게 할것인지를 셋팅한다.

    - ***legend.layout***

      > The layout of the legend items. Can be one of horizontal or vertical or proximate. When proximate, the legend items will be placed as close as possible to the graphs they're representing, except in inverted charts or when the legend position doesn't allow it.
      >
      > 
      >
      > 범례 항목의 레이아웃. `horizontal` 또는 `vertical` 또는 proximate 중 하나 일 수 있습니다. proximate(근사) 할 때, 범례 항목은 그들이 나타내는 그래프에 최대한 가깝게 배치됩니다 (역전 차트 또는 범례 위치에서 허용하지 않는 경우 제외).

      - layout을 결정하는데 기본은 horizontal(수평)으로 설정되어 있다.

        [vertical demo](<https://jsfiddle.net/gh/get/library/pure/highcharts/highcharts/tree/master/samples/highcharts/legend/layout-vertical/>) 에 가보면 x, y 좌표를 이용해서 위치를 조정할 수도 있다.
        [proximate(근사)](<https://jsfiddle.net/gh/get/library/pure/highcharts/highcharts/tree/master/samples/highcharts/legend/layout-proximate>)에 가보면 범례들이 그래프와 최대한 가깝게 배치된걸 확인 가능

        
