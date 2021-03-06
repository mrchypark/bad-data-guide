# 잘못된 데이터에 대한 Quartz 가이드(on-going)

** 실제 데이터에 나타나는 문제에 대한 철저한 참고 자료 및 해결 방법에 대한 제안 **

기자로서 당신의 세계는 데이터로 가득 차 있습니다. 그리고 그 데이터에는 많은 문제가 있습니다. 이 가이드는 데이터 작업시 발생할 수있는 여러 가지 문제에 대한 철저한 설명과 제안 된 솔루션을 제공합니다.

이러한 문제의 대부분을 해결할 수 있습니다. 그 중 일부는 해결할 수 없으며 이는 데이터를 사용하지 말아야 함을 의미합니다. 다른 것들은 해결할 수 없지만 예방 조치를 취하면 데이터를 계속 사용할 수 있습니다. 이러한 모호성을 허용하기 위해이 가이드는 문제 해결에 가장 적합한 사람, 즉 당신, 출처, 전문가 등으로 구성됩니다. 각 문제에 대한 설명에서 해당 사람이 무엇을해야하는지에 대한 제안을 찾을 수도 있습니다 너를 도울 수 없어.

이러한 모든 문제에 대해 발생할 수있는 모든 데이터 세트를 검토 할 수는 없습니다. 그렇게하려고하면 결코 출판 된 것을 얻지 못할 것입니다. 그러나 당신이 겪을 가능성이있는 이슈에 익숙해지면 실수를하게하기 전에 문제를 식별 할 수있는 더 나은 기회를 갖게됩니다.

이 가이드에 대해 궁금한 점이 있으면 [Chris] (mailto : c@qz.com)로 이메일을 보내주십시오. 행운을 빕니다!

이 저작물은 [Creative Commons Attribution-NonCommercial 4.0 국제 라이선스] (http://creativecommons.org/licenses/by-nc/4.0/)에 따라 사용이 허여됩니다. 풀 요청을 보내십시오!

# 번역

* [중국어] (http://cn.gijn.org/2016/01/10/quartz%E5%9D%8F%E6%95%B0%E6%8D%AE%E6%8C%87%E5%8D % 97 % E7 % B2 % BE % E9 % 80 % 89 % EF % BC % 9A % E5 % A4 % 84 % E7 % 90 % 86 % E6 % 95 % B0 % E6 % 8D % AE % E7 % 9A % 84 % E6 % AD % A3 % E7 % A1 % AE % E6 % 96 % B9 % E5 % BC % 8F % E4 % B8 % 80 % E8 % A7 % 88 /
* [스페인어] (http://es.schoolofdata.org/guia-quartz/)

이 가이드를 귀하의 언어로 번역하고 싶습니까? [Chris] (mailto : c@qz.com)에게 이메일을 보내 번역문을 추가하십시오.

# 색인

## 소스가 해결해야 할 문제

* [값 빠뜨림] (# 값이 누락 됨)
* [0은 누락 된 값을 바꿉니다.] (# 제로 대체 - 누락 값)
* [데이터가 누락되었음을 알고 있습니다] (# data-are-missing-you-should-be-there)
* [행 또는 값이 중복 됨] (행 또는 값 중복)
* [철자가 맞지 않음] (# 철자가 일치하지 않음)
* [이름 순서가 맞지 않음] (# 이름 순서가 일치하지 않음)
* [날짜 형식이 일치하지 않음] (날짜 형식 - 일치하지 않음)
* [단위는 지정되지 않음] (단위가 지정되지 않음)
* [카테고리가 잘못 선택되었습니다] (# 카테고리가 잘못 선택됨)
* [필드 이름이 모호합니다] (# 필드 이름이 모호합니다)
* [출처는 문서화되어 있지 않습니다.] (출처 : not-not-documented)
* [수상한 가치 존재 함] (의심스러운 가치 존재)
* [데이터가 너무 거친 경우] (# 데이터가 너무 거친 경우)
* [합계는 게시 된 집계와 다릅니다] (# totals-different-from-published-aggregates)
* [스프레드 시트의 행은 65536 개] (스프레드 시트가있는 행은 65536 행)
* [스프레드 시트에는 255 개의 열이 있습니다.] (스프레드 시트에는 255 개의 열이 있음)
* [스프레드 시트의 날짜는 1900, 1904, 1969 또는 1970입니다 (스프레드 시트 날짜는 1900-1904-1969 또는 1970)
* [텍스트는 숫자로 변환되었습니다.] (숫자로 변환 된 # 텍스트)
* [숫자는 텍스트로 저장되었습니다] (텍스트로 저장된 숫자)

## 해결해야 할 문제

* [글자가 깨졌습니다] (글자가 깨졌습니다)
* [줄 끝 문자가 왜곡됩니다] (# 줄 끝 문자가 깨졌습니다)
* [데이터는 PDF 형식입니다] (pdf 형식의 데이터)
* [너무 세분화 된 데이터] (너무 세분화 된 데이터)
* [데이터는 인간에 의해 입력되었습니다] (# data-were-by-humans)
* [데이터는 서식 및 주석과 혼합되어 있습니다] (# 데이터 - 혼합 및 서식 및 주석)
* [집계는 누락 된 값으로 계산되었습니다] (누락 된 값에 대해 계산 된 집계 수)
* [샘플은 랜덤하지 않습니다] (# 샘플 - 아닌 - 랜덤)
* [여백 오차가 너무 큽니다] (오류 마진의 # margin-too-too)
* [여백 오차는 알 수 없음] (# 오차 한계 - 알려지지 않음)
* [샘플 바이어스 됨] (# 샘플 바이어스 됨)
* [데이터가 수동으로 편집되었습니다] (# 수동으로 편집 된 데이터)
* [인플레이션으로 인해 데이터가 왜곡됩니다] (인플레이션 - 왜곡 - 데이터)
* [자연 / 계절 변화에 따라 데이터가 왜곡됩니다] (# naturalseasonal-variation-skews-the-data)
* [시간 프레임이 조작되었습니다] (# timeframe-has-been-manipulated)
* [참조 프레임이 조작되었습니다] (# 참조 프레임이 조작되었습니다)

## 타사 전문가가 해결해야 할 문제가 있음

* [저자는 신뢰할 수 없다] (# author-is-untrustworthy)
* [수집 프로세스가 불투명] (# collection-process-is-opaque)
* [비현실적인 정확성을 주장하는 데이터] (# data-assert - 비현실적인 정밀도)
* [설명 할 수없는 특이 치 (outexplicable outliers)가있다] (설명 할 수없는 이상 치)
* [인덱스 변형 기본 마스크] (# -in-index-masks-underlying-variation)
* [결과가 해킹되었습니다.] (# 결과가 해킹되었습니다.)
* [벤 포드의 법은 실패합니다] (# 벤 포드 법은 실패합니다)
* [참기 좋다] (너무 좋았다)

## 프로그래머가 해결하는 데 도움이되는 이슈

* [데이터가 잘못된 카테고리 또는 지역에 집계됩니다.] (# 데이터가 합계가 잘못된 카테고리 또는 지역)
* [스캔 한 문서에 데이터 있음] (스캔 한 데이터 수)

# 모든 문제의 상세 목록

## 소스가 해결해야 할 문제

### 값이 누락되었습니다.

그들이 의미하는 바를 모르는 경우를 제외하고는 모든 데이터 세트에서 공백 또는 "null"값을주의하십시오. 데이터가 연간 인 경우 해당 연도의 값이 수집되지 않았습니까? 설문 조사 일 경우 응답자가 질문에 답변하지 않았습니까?

가치가없는 데이터로 작업 할 때는 언제든지 "이 값의 부재가 의미하는 바를 알고 있습니까?"라고 자문해야합니다. 대답이 아니오이면 출처를 물어보십시오.

### 0은 누락 된 값을 대체합니다.

누락 된 값보다 나쁜 것은 임의의 값이 대신 사용될 때입니다. 이는 인간이 의미를 생각하지 않은 결과이거나 Null 값을 처리하는 방법을 모르는 자동화 된 프로세스의 결과로 발생할 수 있습니다. 어떤 경우에도 일련의 숫자에 0이 표시되면 그 값이 실제로 '0'인지 또는 '아무 것도'가 아닌지 스스로에게 물어야합니다. (`-1`은이 방법으로 사용되기도합니다.) 확실하지 않다면 소스를 물어보십시오.

'0'이 다른 식으로 표현 될 수있는 다른 비 숫자 값에 대해서도 동일한주의를 기울여야합니다. 예를 들어 날짜에 대한 거짓 "0"값은 종종 [1970-01-01T00 : 00 : 00Z] 또는 [1969-12-31T24 : 59 : 59Z]로 표시됩니다 [타임 스탬프의 유닉스 신기원] (https : //en.wikipedia.org/wiki/Unix_time#Encoding_time_as_a_number). 위치에 대한 거짓 "0"은 바로 남쪽의 대서양에있는 지점 인 '0 ° 00'00.0'N + 0 ° 00'00.0 'E'또는 간단히 '0 ° N 0 ° E'로 표현 될 수 있습니다 가나는 [Null Island] (https://en.wikipedia.org/wiki/Null_Island)라고도합니다.

참조 :

* [수상한 가치 존재 함] (의심스러운 가치 존재)
* [스프레드 시트의 날짜는 1900, 1904, 1969 또는 1970입니다 (스프레드 시트 날짜는 1900-1904-1969 또는 1970)

### 데이터가 누락되었습니다. 알고 있어야합니다.

때로는 데이터가 누락되어 데이터 세트 자체에서 알 수 없지만 데이터가 무엇을 의미하는지 알기 때문에 데이터 세트 자체에서 알 수는 있습니다. 미국을 다루는 데이터 세트가있는 경우 50 개 주를 모두 확인할 수 있는지 확인할 수 있습니다. (데이터 집합에 푸에르토 리코가 포함 된 경우 [영토] (https://en.wikipedia.org/wiki/Territories_of_the_United_States) -50은 올바른 번호가 아닙니다. 데이터 집합을 다루는 경우 야구 선수들에게 당신이 기대하는 팀 수를 가지고 있는지 확인하십시오. 알고있는 몇 명의 선수가 포함되어 있는지 확인하십시오. 누락 된 부분이 있으면 직감을 신뢰하고 출처를 다시 확인하십시오. 데이터의 우주는 생각보다 작을 수 있습니다.

### 행 또는 값이 중복됩니다.

데이터 세트에 동일한 행이 두 번 이상 나타나는 경우 이유를 찾아야합니다. 때때로 전체 행 일 필요는 없습니다. 일부 캠페인 재무 데이터에는 원래 거래와 동일한 고유 식별자를 사용하는 '수정'이 포함됩니다. 그 사실을 모르는 경우 데이터로 수행 한 계산이 잘못되었습니다. 뭔가 고유 한 것처럼 보이는 경우 그것이 맞는지 확인하십시오. 발견하지 못했다면 출처에게 질문하십시오.

### 철자가 일치하지 않습니다.

맞춤법 검사는 데이터가 손으로 컴파일되었는지 알려주는 가장 확실한 방법 중 하나입니다. 사람들의 이름 만 보는 것이 아니라 철자법 오류를 발견하기가 가장 어려운 곳입니다. 대신 도시 이름이나 주마다 일관성이없는 장소를 찾으십시오. ( '로스 엔젤 로스'는 흔히 볼 수있는 실수 중 하나입니다.) 만약 당신이 그것들을 발견한다면, 데이터가 손으로 편집되거나 편집되었다는 것을 확신 할 수 있습니다. 그리고 그것은 항상 그것에 회의적인 이유입니다. 손으로 편집 한 데이터는 실수가 발생할 가능성이 가장 큽니다. 그렇다고해서 실수로 수정하거나보고 할 때 실수를 수정해야 할 수도 있습니다.

[텍스트 클러스터링] (https://github.com/OpenRefine/OpenRefine/wiki/Clustering) [OpenRefine 's] (http://openrefine.org/) 유틸리티를 사용하면 일치하지 않는 값 사이의 유사성을 제안하여 맞춤법 교정 프로세스를 간소화 할 수 있습니다 (예 : '로스 앤젤레스'와 '로스 앤젤레스'). 그러나 [변경된 사항을 문서화] (https://github.com/OpenRefine/OpenRefine/wiki/Exporters)하여 [적절한 데이터 출처] (출처가 명시되지 않음)를 보장해야합니다.

참조 :

* [데이터는 인간에 의해 입력되었습니다] (# data-were-by-humans)

### 이름 순서가 일치하지 않습니다.

데이터에 중동 또는 동아시아 이름이 있습니까? 성이 항상 같은 장소에 있다고 확신합니까? 데이터 집합에있는 누군가가 [mononym을 사용합니다 (https://en.wikipedia.org/wiki/Indonesian_names#Indonesian_naming_system)를 사용할 수 있습니까? 이것은 데이터 제작자가 습관적으로 잘못한 일들입니다. 임의의 이름 목록 인 인종적으로 다양한 이름의 목록을 가지고 작업한다면`first_name`과`last_name` 컬럼에 합류하는 것이 당신에게 적절한 것이라고 생각하기 전에 적어도 간단한 검토를해야합니다. 게시하십시오.

* [데이터는 인간에 의해 입력되었습니다] (# data-were-by-humans)

### 날짜 형식이 일치하지 않습니다.

9 월의 날짜 :

*`10 / 9 / 15`
*`9 / 10 / 15`

첫 번째 글이 유럽인에 의해 작성되었고 두 번째 글자가 미국인에 의해 작성 되었다면 (둘 다 있습니다) (https://en.wikipedia.org/wiki/Date_format_by_country). 데이터의 역사를 알지 못하면 확실하게 알 수 없습니다. 귀하의 데이터가 어디에서 왔는지를 알고 그것이 같은 대륙의 사람들에 의해 모두 만들어 졌는지 확인하십시오.

* [데이터는 인간에 의해 입력되었습니다] (# data-were-by-humans)
* [출처는 문서화되어 있지 않습니다.] (출처 : not-not-documented)

### 단위가 지정되지 않았습니다.

'무게'와 '비용'은 측정 단위에 관한 정보를 전달하지 않습니다. 미국 내에서 생산 된 데이터가 파운드와 달러 단위로 있다고 가정하는 것이 너무 빠르지 마십시오. 과학 데이터는 종종 측정 항목입니다. 해외 가격은 현지 통화로 지정할 수 있습니다. 데이터가 단위를 철자하지 않으면 출처로 돌아가서 알아보십시오. 그것의 단위를 철자하는 경우에도 항상 시간이 지남에 의미가있을 수 있습니다. 2010 년의 달러는 오늘 달러가 아닙니다. 그리고 [톤] (https://en.wikipedia.org/wiki/Short_ton)은 [톤] (https://en.wikipedia.org/wiki/Long_ton)이나 [톤 (https : /) /en.wikipedia.org/wiki/Tonne).

참조 :

* [필드 이름이 모호합니다] (# 필드 이름이 모호합니다)
* [인플레이션으로 인해 데이터가 왜곡됩니다] (인플레이션 - 왜곡 - 데이터)

### 카테고리가 잘못 선택되었습니다.

단지 '사실'또는 '거짓'이라고 주장하는 가치에주의하십시오. 그러나 실제로 그렇지 않습니다. 이것은 '거절'또는 '무응답'이 유효하고 의미있는 가치가있는 설문 조사의 경우가 종종 있습니다. 또 다른 공통적 인 문제는 '기타'카테고리의 사용입니다. 데이터 세트의 카테고리가 여러 국가와 다른 카테고리 인 경우 그 의미는 무엇입니까? 데이터를 수집 한 사람이 정답을 알지 못했습니까? 그들은 국제 수역에 있었습니까? 외 국인? 피난민?

불량 카테고리는 인위적으로 데이터를 제외 할 수도 있습니다. 이것은 범죄 통계로 자주 발생합니다. FBI는 여러 기간 동안 다양한 방식으로 "강간"범죄를 정의했습니다. 사실, 많은 범죄 학자들이 통계를 전혀 사용하지 말아야한다고 강간이 무엇인지 알아내는 일은 부실한 일이었습니다. 나쁜 정의는 범죄가 예상과 다른 범주에 포함되거나 전혀 집계되지 않았 음을 의미 할 수 있습니다. '인종'이나 '인종'과 같이 정의가 자의적 인 주제로 작업 할 때 예외적으로이 문제를 다루십시오.

### 필드 이름이 모호합니다.

`거주지 '란 무엇입니까? 누군가 살고있는 곳인가, 세금을 내고있는 곳입니까? 도시입니까, 카운티입니까? 데이터의 필드 이름은 우리가 원하는만큼 구체적이지는 않지만 두 가지 이상을 분명히 의미 할 수있는 특정 관심사에 적용해야합니다. 값이 의미하는 바를 정확히 추측하더라도, 모호성으로 인해 데이터를 수집하는 사람이 쉽게 잘못된 값을 입력하게 될 수 있습니다.

### 출처가 문서화되어 있지 않음

데이터는 기업, 정부, 비영리 기관 및 너트 고용 음모론자를 포함하여 다양한 종류의 개인 및 조직에 의해 생성됩니다. 데이터는 설문 조사, 센서 및 위성을 포함하여 다양한 방식으로 수집됩니다. 입력하거나, 탭하거나, 글을 쓸 수 있습니다. 데이터의 출처를 알면 한계에 대한 많은 통찰력을 얻을 수 있습니다.

예를 들어, 설문 조사 데이터는 거의 모든 것이 아닙니다. 센서의 정확도는 다양합니다. 정부는 종종 편견없는 정보를 제공하기를 꺼립니다. 전쟁 지역의 데이터는 전투 선을 넘을 위험이 있기 때문에 지리적 편향성이 클 수 있습니다. 이러한 상황을 악화 시키려면 이러한 서로 다른 소스를 함께 데이지 체인 방식으로 연결해야합니다. 정책 분석가는 종종 정부로부터받은 데이터를 재배포합니다. 의사가 작성한 데이터는 간호사가 입력 할 수 있습니다. 그 사슬의 모든 단계는 오류의 기회입니다. 데이터가 어디서 왔는지 파악하십시오.

참조 :

* [단위는 지정되지 않음] (단위가 지정되지 않음)

### 수상한 가치가 있습니다.

데이터에서 이러한 값 중 하나가 표시되면주의해서 처리하십시오.

번호:

* [`65,535`] (https://en.wikipedia.org/wiki/65535_%28number%29)
* [`255`] (https://en.wikipedia.org/wiki/255_%28number%29)
* [`2,147,483,647`] (https://en.wikipedia.org/wiki/2147483647_%28number%29)
* [`4,294,967,295`] (https://en.wikipedia.org/wiki/4294967295)
* [`555-3485`] (https://en.wikipedia.org/wiki/555_%28telephone_number%29)
*`99999` (또는 9의 다른 긴 시퀀스)
* '00000` (또는 다른 0의 시퀀스)

날짜 :

* [`1970-01-01T00 : 00 : 00Z`] (https://en.wikipedia.org/wiki/Unix_time#Encoding_time_as_a_number)
* [`1969-12-31T23 : 59 : 59Z`] (https://en.wikipedia.org/wiki/Unix_time#Encoding_time_as_a_number)
* [`1900 년 1 월 1 일] (스프레드 시트 날짜는 1900-1904-1969 년 또는 1970 년)
* [`1904 년 1 월 1 일] (스프레드 시트 날짜는 1900-1904-1969 또는 1970)

위치 :

* [`0 ° 00'00.0 "N + 0 ° 00'00.0"E`] (https://en.wikipedia.org/wiki/Null_Island) 또는 단순히 [`0 ° N 0 ° E`] (https : //en.wikipedia.org/wiki/Null_Island)
* 미국 우편 번호`12345` (Schenectady, New York)
* 미국 우편 번호 '90210` (Beverly Hills, CA)

이 숫자들 각각은 사람이나 컴퓨터가 저지른 특별한 오류를 나타냅니다. 당신이 그들을 보는 경우, 그들이 당신이 의미하는 것을 실제로 의미하는지 확인하십시오!

참조 :

* [스프레드 시트의 행은 65536 개] (스프레드 시트가있는 행은 65536 행)
* [스프레드 시트에는 255 개의 열이 있습니다.] (스프레드 시트에는 255 개의 열이 있음)
* [스프레드 시트의 날짜는 1900 또는 1904] (스프레드 시트의 날짜는 1900 또는 1904)

### 데이터가 너무 거칩니다.

주와주의 카운티가 필요합니다. 고용주가 있고 직원이 필요합니다. 그들은 당신에게 몇 년을 보냈지 만 당신은 몇 달을 원합니다. 많은 경우 우리는 우리의 목적을 위해 너무 많이 집계 된 데이터를 얻습니다.

데이터가 병합되면 일반적으로 데이터를 분해 할 수 없습니다. 너무 거친 데이터를 받았다면 소스에 더 구체적인 것을 요청해야합니다. 그들은 그것을 가질 수 없습니다. 그들이 그것을 가지고 있다면, 당신에게 그것을 줄 능력이 없거나 기꺼이하지 못할 수도 있습니다. 지역 수준에서 액세스 할 수없는 수많은 연방 데이터 세트가 존재합니다. 개인 데이터를 통해 고유하게 식별되는 개인의 개인 정보를 보호 할 수는 있습니다. (예를 들어, 텍사스 서부에 거주하는 단일 소말리아 국민). 당신이 할 수있는 것은 묻는 것입니다.

한 번도해서는 안되는 일은 연간 값을 12로 나누어 "월 평균"이라고합니다. 값의 분포를 알지 못하면 그 수는 의미가 없습니다. (아마 모든 인스턴스가 한 달 또는 한 시즌에 발생했을 것입니다. 아마 데이터가 선형 이벤트가 아닌 기하 급수적 인 추세를 따를 수 있습니다.) 잘못되었습니다. 하지 마라.

참조 :

* [너무 세분화 된 데이터] (너무 세분화 된 데이터)
* [데이터가 잘못된 카테고리 또는 지역에 집계됩니다.] (# 데이터가 합계가 잘못된 카테고리 또는 지역)

### 합계는 게시 된 집계와 다릅니다.

긴 FOIA 싸움 후에 당신은 경찰의 사용의 사건의 "완전한"목록을받는다고 상상해보십시오. 열어서 2,467 행을 발견했습니다. 중대한, 그것을 밖으로보고하는 시간. 그리 빠르지는 않습니다. 해당 데이터 세트의 내용을 게시하기 전에 경찰서장이 그의 부서의 무력 사용에 관한 기록을 마지막으로 읽었습니다. 6 주 전에 인터뷰에서 "2,000 회 미만"이라고 말했거나 특정 번호를 지었고 데이터 세트와 일치하지 않는다는 것을 알 수 있습니다.

게시 된 통계와 원시 데이터 간의 이러한 종류의 불일치는 매우 큰 리드 소스가 될 수 있습니다. 종종 대답은 간단합니다. 예를 들어, 주어진 데이터는 그가 말한 것과 동일한 기간을 포함하지 않을 수 있습니다. 그러나 때로는 거짓말로 그들을 잡을 것입니다. 어느 쪽이든 게시 된 숫자가 주어진 데이터의 합계와 일치하는지 확인해야합니다.

### 스프레드 시트에는 65536 개의 행이 있습니다.

구식 Excel 스프레드 시트에 허용 된 최대 행 수는 65,536입니다. 해당 행 수의 데이터 세트를 받으면 잘린 데이터가 거의 확실하게 제공됩니다. 돌아가서 나머지를 요청하십시오. 최신 버전의 Excel에서는 1,048,576 개의 행이 허용되었으므로 한도에 도달하는 데이터로 작업 할 가능성이 적습니다.

### 스프레드 시트에는 255 개의 열이 있습니다.

Apple의 Numbers 앱은 255 열의 스프레드 시트 만 처리 할 수 ​​있으며, 앱은 사용자에게 경고하지 않고 더 많은 열을 가진 파일을 자릅니다. 정확히 255 열의 데이터 세트를 수신 한 경우 파일이 열렸거나 Numbers로 변환되었는지 확인하십시오.

### 스프레드 시트의 날짜는 1900 년, 1904 년, 1969 년 또는 1970 년입니다.

모호하지 않은 이유로 Excel의 기본 날짜는 '19 1 월 1 일 '입니다. * Mac에서 Excel을 사용하지 않는 한, 1904 년 1 월 1 일입니다. Excel의 데이터를 잘못 입력하거나 계산하여이 두 날짜 중 하나로 끝나는 다양한 방법이 있습니다. 데이터에서 해당 항목을 발견하면 문제 일 수 있습니다.

많은 데이터베이스와 응용 프로그램은 종종 [1970-01-01T00 : 00 : 00Z] 또는 [1969-12-31T23 : 59 : 59Z]의 날짜를 생성합니다 [타임 스탬프의 유닉스 시대] (https : //en.wikipedia .org / wiki / Unix_time # Encoding_time_as_a_number). 즉, 시스템이 빈 값이나 '0'값을 날짜로 표시하려고 할 때 발생합니다.

### 텍스트가 숫자로 변환되었습니다.

모든 숫자가 숫자는 아닙니다. 예를 들어, 미국 센서스 국은 "FIPS 코드"를 사용하여 미국의 모든 장소를 식별합니다. 이 코드는 다양한 길이이며 숫자입니다. 그러나 그들은 숫자가 아닙니다. '037'은 로스 앤젤레스 카운티의 FIPS 코드입니다. 숫자 '37'이 아닙니다. 그러나 '37'이라는 숫자는 노스 캐롤라이나에서 유효한 FIPS 코드입니다. Excel 및 기타 스프레드 시트는 종종 숫자가 숫자라고 가정하고 맨 앞의 0을 제거하는 실수를 범합니다. 다른 파일 형식으로 변환하거나 다른 데이터 형식으로 병합하려고하면 모든 종류의 문제가 발생할 수 있습니다. 이것이 주어지기 전에 일어난 일을주의하십시오.

### 숫자가 텍스트로 저장되었습니다.

스프레드 시트로 작업 할 때 숫자는 원하지 않는 형식의 텍스트로 저장 될 수 있습니다. 이는 스프레드 시트가 데이터를 재사용 할 수 있도록하기보다는 데이터를 표시하도록 최적화 된 경우에 자주 발생합니다. 예를 들어 백만 달러를 숫자 "1000000"으로 표시하는 대신 셀에 쉼표, 단위 및 공백을 문자로 입력하여 "1,000,000"또는 "1 000 000"또는 "USD 1,000,000"문자열을 포함 할 수 있습니다. Excel에서는 내장 함수를 사용하여 간단한 경우를 처리 할 수 ​​있지만 숫자로 인식 될 수있을만큼 셀이 깨끗해질 때까지 수식을 사용하여 문자를 제거해야하는 경우가 있습니다. 형식을 지정하지 않고 숫자를 저장하고 열 이름이나 메타 데이터에 지원 정보를 포함하는 것이 좋습니다.

## 해결해야 할 문제

### 텍스트가 왜곡됩니다.

모든 문자는 컴퓨터로 숫자로 표시됩니다. 인코딩 문제는 텍스트가 특정 숫자 집합 ( "인코딩"이라고 함)으로 표현되고 그 내용을 모를 때 발생하는 문제입니다. 이로 인해 데이터의 텍스트가 가비지처럼 보이거나 다음과 같이 나타나는 [mojibake] (https://en.wikipedia.org/wiki/Mojibake) 현상이 발생합니다.

대다수의 경우 텍스트 편집기 또는 스프레드 시트 응용 프로그램이 올바른 인코딩을 알아낼 것입니다. 그러나 나사를 조이면 중간에 이상한 문자가있는 누군가의 이름을 게시 할 수 있습니다. 귀하의 출처는 귀하의 데이터가 어떤 인코딩이되어 있는지를 알려줄 수 있어야합니다. 그들이 신뢰할 수있는 추측의 방법이없는 경우에는 귀하의 데이터가 무엇인지 알려줄 수 있어야합니다. 프로그래머에게 물어보십시오.

### 줄 끝이 왜곡됩니다.

모든 텍스트와 CSV와 같은 "텍스트 데이터"파일은 보이지 않는 문자를 사용하여 선의 끝을 나타냅니다. Windows, Mac 및 Linux 컴퓨터는 역사적으로 이러한 줄 끝 문자가 무엇인지에 대해 동의하지 않았습니다. 한 운영 체제에 저장된 파일을 다른 운영 체제에서 열려고하면 Excel이나 다른 응용 프로그램이 줄 바꿈을 제대로 식별하지 못할 수 있습니다.

일반적으로이 파일은 범용 텍스트 편집기에서 파일을 열고 다시 저장하기 만하면 쉽게 해결할 수 있습니다. 파일이 매우 큰 경우 명령 줄 도구를 사용하거나 프로그래머의 도움을 받아야 할 수도 있습니다. 이 문제에 대한 자세한 내용은 [여기] (https://nicercode.github.io/blog/2013-04-30-excel-and-line-endings/)에서 확인할 수 있습니다.

### 데이터는 PDF 형식입니다.

엄청난 양의 데이터 (특히 정부 데이터)는 PDF 형식으로 만 제공됩니다. PDF에 실제 텍스트 데이터가있는 경우 추출하기위한 몇 가지 좋은 옵션이 있습니다. ([스캔 한 문서] (# 스캔 한 문서 데이터)가 다른 문제 인 경우) 우수한 무료 도구는 [Tabula] (http://tabula.technology/)입니다. 그러나 Adobe Creative Cloud를 사용하는 경우 Acrobat Pro에 액세스 할 수 있습니다. Acrobat Pro는 PDF의 표를 Excel로 내보낼 수있는 뛰어난 기능을 제공합니다. 두 솔루션 모두 PDF에서 대부분의 표 형식 데이터를 추출 할 수 있어야합니다.

참조 :

* [스캔 한 문서에 데이터 있음] (스캔 한 데이터 수)

### 데이터가 너무 세분합니다.

이것은 [데이터가 너무 거친 것]과 반대입니다 (# data-are-too-coarse). 이 경우에는 카운티가 있지만 주를 원하거나 월이 있지만 몇 년이 필요합니다. 다행히도 이것은 대개 간단합니다.

Excel 또는 Google 문서 도구의 피벗 테이블 기능을 사용하거나 SQL 데이터베이스를 사용하거나 사용자 지정 코드를 작성하여 데이터를 집계 할 수 있습니다. 피벗 테이블은 모든 기자가 배워야 할 멋진 도구이지만 한계가 있습니다. 예외적으로 큰 데이터 세트 나 특이한 그룹에 대한 집계를 위해서는 프로그래머에게 물어보아야하며 검증 및 재사용이 더 쉬운 솔루션을 만들 수 있습니다.

참조 :

* [데이터가 너무 거친 경우] (# 데이터가 너무 거친 경우)
* [데이터가 잘못된 카테고리 또는 지역으로 집계됩니다] (# 데이터 집계가 잘못된 카테고리 또는 지역).

### 데이터는 인간에 의해 입력되었습니다.

인적 데이터 입력은 흔히 발생하는 문제로서 여기에 설명 된 다른 문제 중 적어도 10 가지에서 언급됩니다. 유효성 검사없이 단일 인간이 데이터를 입력하는 것보다 데이터를 망칠 더 나쁜 방법은 없습니다. 예를 들어, 일리노이 주 쿡 카운티 (Que County)에 대한 완전한 개 라이센스 데이터베이스를 한 번 취득했습니다. 목록에있는 품종을 선택하기 위해 개를 등록하는 사람을 요구하는 대신, 시스템 작성자는 입력 할 텍스트 필드 만 입력하면됩니다. 결과적으로이 데이터베이스는 "치와와"의 철자를 250 가지 이상 포함하고 있습니다. 사용 가능한 최상의 도구가 있더라도이 지저분한 데이터는 저장할 수 없습니다. 그들은 사실 무의미합니다. 이것은 개 데이터와 함께 중요하지 않지만 부상당한 병사 또는 주식 시세 표시기로 발생하는 것을 원하지 않습니다. 인간이 입력 한 데이터를 조심하십시오.

### 데이터는 서식 및 주석과 혼합됩니다.

HTML 및 XML과 같은 복잡한 데이터 표현은 데이터와 형식을 명확하게 구분할 수 있지만 스프레드 시트와 같은 데이터를 표로 표현하는 일반적인 경우에는 해당되지 않습니다. 그러나 사람들은 여전히 ​​시도합니다. 스프레드 시트로 제공되는 데이터의 일반적인 문제점은 데이터의 처음 몇 행은 실제로 열 머리글 또는 데이터 자체가 아닌 데이터에 대한 설명 또는 메모입니다. 키 또는 데이터 사전은 스프레드 시트의 중간에 배치 될 수도 있습니다. 헤더 행이 반복 될 수 있습니다. 또는 스프레드 시트에는 다른 시트로 분리되지 않고 같은 시트에 여러 테이블 (서로 다른 열 머리글이있을 수 있음)이 차례로 포함됩니다.

이 모든 경우에 주요 해결책은 단순히 문제를 식별하는 것입니다. 분명히 이러한 종류의 문제가있는 스프레드 시트에 대한 분석을 수행하려고 시도하는 것은 실패 할 것이며 때로는 명백하지 않은 이유로 실패 할 것입니다. 처음으로 새로운 데이터를 볼 때 여분의 헤더 행이나 데이터 사이에 삽입 된 다른 형식화 ​​문자가 없는지 항상 확인하는 것이 좋습니다.

### 누락 된 값에 대해 집계가 계산되었습니다.

100 행의 데이터 세트와 '비용'이라는 열을 상상해보십시오. 50 행에서 '비용'열은 비어 있습니다. 해당 열의 평균은 얼마입니까? `sum_of_cost / 50` 또는`sum_of_cost / 100`입니까? 확실한 답은 없습니다. 일반적으로 데이터가 누락 된 열에서 집계를 계산하려면 먼저 누락 된 행을 필터링하여 안전하게 수행 할 수 있지만 행이 누락 된 두 개의 열에서 집계를 비교하지 않도록주의하십시오! 경우에 따라 누락 된 값은 '0'으로 합법적으로 해석 될 수 있습니다. 확실하지 않으면 전문가에게 질문하거나하지 마십시오.

이것은 분석에서 발생할 수있는 오류이지만 다른 사람들이 작성하여 전달할 수있는 오류이기도하므로 이미 계산 된 집계를 사용하여 데이터가 제공되는 경우주의하십시오.

참조 :

* [값 빠뜨림] (# 값이 누락 됨)
* [0은 누락 된 값을 바꿉니다.] (# 제로 대체 - 누락 값)

### 샘플은 랜덤하지 않습니다.

무작위 표본 추출 오류는 설문 조사 나 다른 표본 추출 된 데이터 집합이 의도적으로 또는 우발적으로 전체 인구를 다루지 못할 때 발생합니다. 이것은 시간대에서부터 응답자의 모국어에 이르기까지 다양한 이유로 발생할 수 있으며 사회학 연구에서 공통된 오류 원인입니다. 연구자가 완전한 데이터 세트를 가지고 있으며 일부만 사용하도록 선택한 경우와 같이 덜 분명한 이유 때문에 발생할 수도 있습니다. 어떤 이유로 든 원본 데이터 세트가 불완전한 경우 샘플에서 추출한 결론이 정확하지 않습니다. 무작위가 아닌 샘플을 수정하기 위해 할 수있는 유일한 방법은 해당 데이터를 사용하지 않는 것입니다.

참조 :

* [샘플 바이어스 됨] (# 샘플 바이어스 됨)

### 여백 오차가 너무 큼

매우 큰 여백 오류가있는 숫자의 무반사 사용보다 더 많은보고 오류를 발생시키는 다른 단 하나의 문제는 알지 못합니다. 환경부 장관은 일반적으로 설문 조사 데이터와 관련이 있습니다. 기자가 만날 가능성이 가장 높은 곳은 폴링 데이터 또는 미국 인구 통계국 (American Census Bureau)의 [American Community Survey] (https://www.census.gov/programs-surveys/acs/) 데이터를 사용할 때입니다. 환경부는 가능한 실제 값의 범위를 측정합니다. 숫자 ( '400 +/- 80') 또는 전체의 백분율 ( '400 +/- 20 %')로 표시 될 수 있습니다. 관련 인구가 적을수록 환경부는 더 커질 것이다. 예를 들어, 2014 년 5 년 ACS 추정치에 따르면 뉴욕에 거주하는 아시아 인은 '1,106,989 +/3,526` (0.3 %)입니다. 필리핀 인은`71,969 +/- 3,088` (4.3 %)이다. 사모아의 수는`203 +/- 144` (71 %)입니다.

처음 두 숫자는보고하는 것이 안전합니다. 세 번째 번호는 게시 된보고에서 사용해서는 안됩니다. 숫자가 사용하기에는 정확하지 않을 때에 대한 규칙은 없지만, 경험상 10 % 이상의 환경부 (MOE) 번호를 사용하는 것에 대해서는 신중해야합니다.

참조 :

* [여백 오차는 알 수 없음] (# 오차 한계 - 알려지지 않음)

### 오류의 한계가 알려지지 않았습니다.

때로는 문제가 오류의 마진이 [너무 큽니다] (오류 마진의 # margin-too-too)가 아니며, 처음에는 무엇인지 파악하는 데 아무도 귀찮은 사람이 아닙니다. 이것은 비과학적인 여론 조사의 한 가지 문제입니다. 환경부 (MOE)를 계산하지 않으면 결과가 얼마나 정확한지 알 수 없습니다. 일반적으로 설문 조사의 데이터가있을 때마다 환경부 (MOE)가 무엇인지 물어야합니다. 근원이 당신을 말할 수없는 경우에, 그 자료는 어떤 심각한 분석든지를 위해 사용의 값이있는 아마 아마이지 않는다.

참조 :

* [여백 오차가 너무 큽니다] (오류 마진의 # margin-too-too)

### 샘플이 바이어스 됨

[무작위가 아닌 샘플] (# sample-is-not-random)처럼, 편향된 샘플은 샘플링이 실행되는 방법에 대한주의 부족 때문에 생깁니다. 또는 고의적으로 잘못 설명하는 것. 샘플은 인터넷에서 수행 되었기 때문에 편향 될 수 있으며 가난한 사람들은 부자만큼 자주 인터넷을 사용하지 않습니다. 설문 조사 결과를 왜곡 할 수있는 인구의 비례 세그먼트를 커버하도록주의 깊게 가중치를 주어야합니다. 이 작업을 완벽하게 수행하는 것이 거의 불가능하므로 종종 잘못 수행됩니다.

참조 :

* [샘플은 랜덤하지 않습니다] (# 샘플 - 아닌 - 랜덤)

### 데이터는 수동으로 편집되었습니다.

수동 편집은 사실 이후에 발생하는 것을 제외하고는 [인간에 의해 입력 된 데이터] (인간에 의해 입력 된 데이터)와 거의 동일한 문제입니다. 사실, 데이터는 종종 사람이 입력 한 데이터를 수정하기 위해 수동으로 편집됩니다. 편집자가 원본 데이터에 대한 완전한 지식이없는 경우 문제가 발생하기 시작합니다. 한 번 누군가가 "Smit"에서 "Smith"까지 데이터 세트의 이름을 자발적으로 "수정"하는 것을 보았습니다. 그 사람의 이름이 정말로`스미스`였습니까? 나는 모른다. 그러나 나는 가치가 이제는 문제라는 것을 알고있다. 그러한 변화에 대한 기록이 없다면, 그것이 무엇이어야 하는지를 확인하는 것은 불가능합니다.

수동 편집과 관련된 문제는 데이터에 [잘 문서화 된 출처]가 있는지 항상 확인해야하는 이유 중 하나입니다 (출처가 문서화되지 않음). 출처가 부족하면 누군가가 원숭이와 함께했을 수도 있다는 좋은 징후가 될 수 있습니다. 학계 및 정책 분석가들은 종종 정부와 원숭이로부터 데이터를 얻은 다음 언론인에게 배포합니다. 변경 사항에 대한 기록이 없으면 변경 사항이 합리화되었는지 여부를 알 수 없습니다. 가능할 때마다 항상 * 기본 소스 * 또는 적어도 가능한 가장 오래된 버전을 얻고 그로부터 자신의 분석을 시도하십시오.

참조 :

* [출처는 문서화되어 있지 않습니다.] (출처 : not-not-documented)
* [데이터는 인간에 의해 입력되었습니다] (# data-were-by-humans)

인플레이션으로 인해 데이터가 왜곡됩니다.

통화 팽창은 시간이 지남에 따라 돈이 가치가 있음을 의미합니다. 숫자를보고 만 인플레이션을 조정했는지 알 수있는 방법이 없습니다. 데이터를 얻었을 때 데이터가 조정되었는지 확실하지 않으면 소스를 확인하십시오. 그렇지 않은 경우 조정을 수행하기를 원할 것입니다. 이 [인플레이션 조정자] (http://inflation-adjust.herokuapp.com/)는 시작할 수있는 좋은 곳입니다.

참조 :

* [자연 / 계절 변화에 따라 데이터가 왜곡됩니다] (# nationalseasonal-variation-skews-the-data)

자연적 / 계절적 변화로 인해 데이터가 왜곡됩니다.

많은 유형의 데이터가 근본적인 원인에 따라 자연스럽게 변동합니다. 가장 잘 알려진 예는 계절에 따라 변동하는 고용입니다. 경제학자들은 이러한 변화를 보상하기위한 다양한 방법을 개발했습니다. 이러한 방법의 세부 사항은 특별히 중요하지 않지만 사용중인 데이터가 "계절적으로 조정"되었는지 여부를 아는 것이 중요합니다. 그들이 가지고 있지 않고 월별 고용을 비교하고 싶다면 아마 당신의 출처에서 조정 된 데이터를 얻고 싶을 것입니다. (스스로 조정하는 것은 인플레이션보다 훨씬 어렵습니다.)

참조 :

* [인플레이션으로 인해 데이터가 왜곡됩니다] (인플레이션 - 왜곡 - 데이터)

### 시간 프레임이 조작되었습니다.

소식통은 특정 시간에 멈추거나 시작하는 데이터를 제공함으로써 실수로 또는 의도적으로 세상을 허위 진술 할 수 있습니다. 유력한 예를 보려면 2015 년에 널리보고 된 "국가 범죄 파"를 참조하십시오. 범죄가 발생하지 않았습니다. 지난 몇 년과 비교했을 때 특정 도시에는 일련의 급증이있었습니다. 기자가 폭력 범죄가 미국 전역에서 사실상 10 년 전보다 더 높았다는 것을 알았을 때보 다 더 넓은 기간을 조사했다면. 그리고 20 년 전에는 거의 두 배가되었습니다.

제한된 기간을 다루는 데이터가있는 경우 데이터가있는 첫 번째 기간에 계산을 시작하지 마십시오. 데이터를 몇 년 (또는 몇 개월 또는 며칠) 시작하면 추가 데이터 요소가 하나만 있으면 비교할 수없는 비교를하지 않을 것이라는 확신을 가질 수 있습니다.

참조 :

* [참조 프레임이 조작되었습니다] (# 참조 프레임이 조작되었습니다)

### 참조 프레임이 조작되었습니다.

범죄 통계는 종종 범죄가 매우 많이 발생한 연도와 비교하여 정치적 목적으로 조작됩니다. 이는 변화 (2004 년 이후 60 % 하락) 또는 지수 (2004 년 = 100)를 통해 나타낼 수 있습니다. 이 두 경우 모두 2004 년은 비교하기 적합한 연도 일 수도 있고 아닐 수도 있습니다. 그것은 비정상적으로 높은 범죄의 해 였을 수 있습니다.

이것은 장소를 비교할 때도 발생합니다. 한 국가를보기 좋게 보이게하려는 경우 단순히 최선을 다한 국가와 관련하여 해당 국가의 데이터를 표현하기 만하면됩니다.

이 문제는 사람들이 강한 편견을 가지고있는 대상에서 자란 경향이 있습니다. ( "내가 생각한 것처럼, 범죄가 일어났습니다!") 가능하면 언제나 숫자가 어떻게 다른지를보기 위해 여러 가지 출발점에서의 비율을 비교해보십시오. 그리고 당신이하는 일은, 당신이 중요하다고 생각하는 점을 만들기 위해이 기법을 직접 사용하지 마십시오. 그건 용납 할 수없는 일이다.

참조 :

* [시간 프레임이 조작되었습니다] (# timeframe-has-been-manipulated)

## 타사 전문가가 해결해야 할 문제가 있음

### 저자는 신뢰할 수 없습니다.

때때로 당신이 가지고있는 유일한 데이터는 당신이 의존하지 않는 소스로부터 온 것입니다. 어떤 경우에는 괜찮습니다. 총을 몇 개 만들었는지 알 수있는 유일한 사람은 총 제조 업체입니다. 그러나 의심스러운 제조사의 데이터가있는 경우 다른 전문가와 항상 확인하십시오. 더 나은 방법은 두세 가지로 확인하십시오. 확실한 증거가 없다면 편향된 출처의 데이터를 게시하지 마십시오.

### 콜렉션 프로세스가 불투명합니다.

허위 가정, 오류 또는 철저한 거짓 정보가 이러한 데이터 수집 프로세스에 도입되는 것은 매우 쉽습니다. 이러한 이유로 사용 된 방법이 투명해야합니다. 데이터 세트가 어떻게 수집되었는지 정확히 알 수는 없지만 문제의 징후는 [비현실적인 정확성을 주장하는] 숫자 (# 데이터 주장 - 비현실적인 정밀도)와 [실제하기에는 너무 좋은] 데이터를 포함 할 수 있습니다 ( #사실 너무 좋은).

때로는 기원 이야기가 단지 비린내 일 수도 있습니다. 그러한 학자들은 시카고 남쪽에서 활동중인 50 명의 갱단과 정말로 인터뷰를 했습니까? 데이터가 수집 된 방식이 의심스럽고 출처가 당신에게 [철저한 기원]을 제공 할 수 없다면 (# 출처는 문서화되지 않음) 다른 전문가와 함께 데이터가 합리적으로 수집 될 수 있는지를 확인해야합니다 그것은 묘사되었다.

참조 :

* [출처는 문서화되어 있지 않습니다.] (출처 : not-not-documented)
* [비현실적인 정확성을 주장하는 데이터] (# data-assert - 비현실적인 정밀도)
* [참기 좋다] (너무 좋았다)

### 데이터가 비현실적인 정밀도를 나타냅니다.

경질 과학을 제외하고는 정확도가 소수점 두 자리 이상으로 측정되는 것이 거의 없습니다. 데이터 세트가 책상에 떨어지면 다른 가치로 추정되는 죽은 공짜 인 7 번째 소수점까지 공장의 배출량을 표시합니다. 그 자체로는 문제가되지 않을 수도 있지만 추정치에 대해 투명해야합니다. 그들은 종종 잘못되었습니다.

설명 할 수없는 특이 치가있다.

나는 최근에 메시지가 인터넷을 통해 다른 목적지에 도달하는 데 걸리는 시간의 데이터 세트를 만들었습니다. 모든 시간은 '0.05'에서 '0.8'초까지 3 번을 제외하고 있었다. 나머지 세 명은 모두`5,000 초 '를 넘었다. 이것은 데이터 생산시에 문제가있는 주요한 적기입니다. 이 특별한 경우에 필자가 작성한 코드의 오류로 인해 다른 모든 메시지가 보내고받는 동안 계속 실패하는 오류가 발생했습니다.

이러한 이상 치는 통계를 크게 망칠 수 있습니다. 특히 평균을 사용하는 경우 더욱 그렇습니다. 새 데이터 집합을 만들 때마다 가장 큰 값과 가장 작은 값을 확인하고 합리적인 범위에 있는지 확인하는 것이 좋습니다. 데이터가이를 정당화하는 경우 [표준 편차] (https://en.wikipedia.org/wiki/Standard_deviation) 또는 [중앙 편차] (https : //en.wikipedia)를 사용하여 통계적으로 더 엄격한 분석을 수행 할 수도 있습니다. org / wiki / Median_absolute_deviation).

이 작업을 수행 할 때의 부수적 인 이점으로, 이상 치는 종종 스토리 리드를 찾는 좋은 방법입니다. 인터넷을 통해 메시지를 보내는 데 오랜 시간이 걸린 국가가 실제로 한 곳이라면 훌륭한 이야기가 될 것입니다.

인덱스는 기본 변형을 가린다.

문제의 추세를 따르기를 원하는 애널리스트는 진행 상황을 추적하기 위해 다양한 가치 지표를 작성합니다. 인덱스를 사용할 때 본질적으로 잘못된 것은 없습니다. 그들은 큰 설명력을 가질 수 있습니다. 그러나 이질적인 조치를 취하는 지표에 대해서는 신중해야합니다.

예를 들어, 유엔 (여성 불평등 지수) (http://hdr.undp.org/en/content/gender-inequality-index-gii)은 평등을 향한 여성의 진보와 관련된 몇 가지 조치를 결합합니다. GII에서 사용 된 조치 중 하나는 "여성 의회 대표"입니다. 세계의 두 나라는 중국과 파키스탄 의회에서 성 평등을 요구하는 법을 제정했다. 결과적으로이 두 국가는 다른 모든 국가와 비슷한 국가보다 훨씬 잘 수행됩니다. 이거 공정한가요? 이 요소에 대해 모르는 사람들에게는 혼란을주기 때문에 중요하지 않습니다. GII 및 유사한 지표는 기본 변수가 예상치 못한 방식으로 지표를 변동시키지 않도록 항상 면밀한 분석과 함께 사용해야합니다.

### 결과가 해킹되었습니다.

P 해킹은 의도적으로 데이터를 변경하거나, 통계 분석을 변경하거나, 통계적으로 중요한 결과를 얻기 위해 결과를 선택적으로보고합니다. 예를 들어 중요한 결과를 얻은 후에는 데이터 수집을 중단하고, 중요한 결과를 얻으려면 관찰을 제거하거나, 많은 분석을 수행하고 중요한 일부만보고하십시오. 이 문제에 대해 [좋은보고] (http://fivethirtyeight.com/features/science-isnt-broken)가있었습니다.

연구 결과를 발표하려면 p- 값이 무엇인지, 그 의미가 무엇인지 파악한 다음 결과에 가치가 있는지 여부에 대한 교육적 결정을 내려야합니다. 기자들이 p- 값을 이해하지 못하기 때문에 많은 쓰레기 연구 ​​결과가 주요 출판물이됩니다.

참조 :

* [여백 오차가 너무 큽니다] (오류 마진의 # margin-too-too)

벤 포드의 법칙이 실패했습니다.

[Benford 's Law] (https://en.wikipedia.org/wiki/Benford's_law)는 작은 숫자 (1, 2, 3)가 숫자의 시작 부분에 큰 숫자 (7 , 8, 9). 이론적으로 Benford의 법칙은 회계 관행이나 선거 결과의 변칙을 발견하는 데 사용될 수 있지만 실제로는 쉽게 오용 될 수 있습니다. 기망하도록 데이터 집합을 만들거나 수정 한 것으로 의심되는 경우 Benford의 법칙은 우수한 첫 번째 테스트이지만 데이터가 조작 된 것으로 결론지기 전에 항상 전문가와 결과를 확인해야합니다.

### 사실 너무 좋은

여론에 대한 세계적인 데이터 세트는 없습니다. 시베리아에 사는 사람들의 정확한 숫자는 아무도 모른다. 범죄 통계는 국경 간 비교가되지 않습니다. 미국 정부는 얼마나 많은 핵분열 물질을 보유하고 있는지 알려주지 않을 것입니다.

당신이 알지 못했던 것을 표현하기위한 모든 데이터를 유의하십시오. 그것은 데이터가 아닙니다. 그것은 누군가의 추정이고 아마도 틀렸을 것입니다. 그런 다음 다시 이야기가 될 수 있으므로 전문가에게 확인하십시오.

## 프로그래머가 해결하는 데 도움이되는 이슈

### 데이터가 잘못된 범주 또는 지역에 집계됩니다.

때로는 귀하의 데이터가 올바른 수준의 세부 사항 (너무 조잡하지 않음) 또는 너무 세분화되지 않은 (너무 세분화 된) 데이터 일 수도 있지만, 네가 원하는 것보다 다른 그룹. 전형적인 예는 도시 지역에서 선호하는 우편 번호로 집계 된 데이터입니다. 많은 경우 소스에서보다 세부적인 데이터를 얻지 않으면 해결할 수없는 문제이지만 데이터가 한 그룹에서 다른 그룹으로 비례 적으로 매핑되는 경우가 있습니다. 이는 프로세스에서 도입 될 수있는 [margin of error] (# margin-of-error-is-too-large)에 대한주의 깊은 이해를 통해서만 수행되어야합니다. 잘못된 그룹에 데이터를 집계 한 경우 프로그래머에게 다시 집계 할 수 있는지 물어보십시오.

참조 :

* [데이터가 너무 거친 경우] (# 데이터가 너무 거친 경우)
* [너무 세분화 된 데이터] (너무 세분화 된 데이터)
* [여백 오차가 너무 큽니다] (오류 마진의 # margin-too-too)

### 스캔 한 문서에 데이터가 있습니다.

FOIA 법률 덕분에 정부는 실제로 원하지 않지만 데이터를 제공해야하는 경우가 많습니다. 이 경우 매우 일반적인 방법은 페이지 스캔 또는 사진을 제공하는 것입니다. 이 파일은 실제 이미지 파일 일 수도 있고, 더 많은 경우 PDF로 모아질 수도 있습니다.

이미지에서 텍스트를 추출하여 다시 데이터로 변환 할 수 있습니다. 이것은 광학 문자 인식 (OCR)이라는 프로세스를 통해 수행됩니다. 현대 OCR은 종종 거의 100 % 정확할 수 있지만 문서의 성격에 따라 다릅니다. OCR을 사용하여 데이터를 추출 할 때마다 원본과 일치하는 결과를 검증하는 프로세스가 필요합니다.

OCR을 위해 문서를 업로드 할 수있는 웹 사이트가 많이 있지만 프로그래머가 특정 문서를 조정할 수있는 무료 도구가 있습니다. 보유하고있는 특정 문서에 가장 적합한 전략이 무엇인지 물어보십시오.

참조 :

* [데이터는 PDF 형식입니다] (pdf 형식의 데이터)
