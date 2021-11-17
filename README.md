# README

```markdown
If..목차로 조금더 편하게 보고 싶다면 [Gabe's Notion](https://www.notion.so/README-46d0652b7a134dc3a2bdec84c92b5fa7) 으로 ~! 😉
```

---

# 1. Preprocessing

---

## 데이터 핸들링 관련

### [Pandas String 데이터 기본 전처리](https://github.com/gabesoon/Data_analysis_Cheatsheet/blob/main/%5BProprocessing%5D%20Pandas%20String%20%EB%8D%B0%EC%9D%B4%ED%84%B0%20%EA%B8%B0%EB%B3%B8%20%EC%A0%84%EC%B2%98%EB%A6%AC.ipynb) 코드 모음 zip

- 상세내용
    
    1)  인덱싱 하기
    
    ```python
    str[ 시작idx : 끝 idx+1 ]
    ```
    
    2)  컬럼내 데이터를 split해서 여러 컬럼으로 만들기 
    
    ```python
    str.split('기준')
    ```
    
    3)  컬럼내 데이터를 split해서 여러 행으로 만들기 
    
    4)  ~로 시작하는 문자열 찾기 : 
    
    ```python
    str.startswith()
    ```
    
    5) ~로 끝나는 문자열 찾기 : 
    
    ```python
    str.endswith()
    ```
    
    6) 데이터 내에 "~ 문자" 가 있는지 찾기 :  
    
    ```python
    str.contains()
    ```
    
    7) 정규표현식으로 조건에 맞는 문자 찾기 : 
    
    ```python
    str.findall()
    ```
    
    8)  특정문자의 idx값 찾기 : 
    
    ```python
    str.find()
    ```
    
    9) 문자값을 원하는 문자열로 바꾸기 : 
    
    ```python
    str.replace()
    ```
    
    10) 원하는 문자열만 추출하기 : 
    
    ```python
    str.extract()
    ```
    
    11) 특정 width만 큼 문자열 값 채우기 : 
    
    ```python
    str.pad() & str.center &  str.zfill()
    ```
    
    12) 문자열 데이터의 공백 제거하기 : 
    
    ```python
    strip()
    ```
    
    13) 대소문자 변경하기 :  
    
    ```python
    str.lower() & str.upper() & swapcase()
    ```
    

### [서로 길이가 다른 list/Series를 DataFrame으로 만들기](https://github.com/gabesoon/Data_analysis_Cheatsheet/blob/main/%5BProprocessing%5D%20%EC%84%9C%EB%A1%9C%20%EA%B8%B8%EC%9D%B4%EA%B0%80%20%EB%8B%A4%EB%A5%B8%20list%20or%20Series%20%EC%97%AC%EB%9F%AC%EA%B0%9C%EB%A5%BC%20%ED%95%A9%EC%B3%90%EC%84%9C%20DataFrame%20%EB%A7%8C%EB%93%A4%EA%B8%B0.ipynb)

---

## Merge 관련

### [시간과 날짜 컬럼 데이터의 병합은 'apply'를 써야 한다.](https://github.com/gabesoon/Python/blob/main/6.%20Preprocessing/03.%20%5B%EB%8D%B0%EC%9D%B4%ED%84%B0%20%ED%8C%8C%ED%8E%B8%ED%99%94%20%EB%AC%B8%EC%A0%9C%5D%20%20%ED%8F%AC%EB%A7%B7%EC%9D%B4%20%EB%8B%A4%EB%A5%B8%20%EB%8D%B0%EC%9D%B4%ED%84%B0%20%EB%B3%91%ED%95%A9(merge)_(1)%20%EC%B0%B8%EC%A1%B0%20%EB%8D%B0%EC%9D%B4%ED%84%B0%EA%B0%80%20%ED%95%84%EC%9A%94%EC%97%86%EB%8A%94%20%EA%B2%BD%EC%9A%B0.ipynb)

### [일정한 패턴이 없거나, 포맷이 다른 데이터 병합은 참고자료를 쓴다.](https://github.com/gabesoon/Python/blob/main/6.%20Preprocessing/04.%20%5B%EB%8D%B0%EC%9D%B4%ED%84%B0%20%ED%8C%8C%ED%8E%B8%ED%99%94%20%EB%AC%B8%EC%A0%9C%5D%20%20%ED%8F%AC%EB%A7%B7%EC%9D%B4%20%EB%8B%A4%EB%A5%B8%20%EB%8D%B0%EC%9D%B4%ED%84%B0%20%EB%B3%91%ED%95%A9(merge)_(2)%20%EC%B0%B8%EC%A1%B0%20%EB%8D%B0%EC%9D%B4%ED%84%B0%EA%B0%80%20%ED%95%84%EC%9A%94%ED%95%9C%20%EA%B2%BD%EC%9A%B0.ipynb)

### [폴더내의 동일한 from의 여러파일을 하나의 DataFrame으로 만들기](https://github.com/gabesoon/Python/blob/main/6.%20Preprocessing/01.%20%5B%EB%8D%B0%EC%9D%B4%ED%84%B0%20%ED%8C%8C%ED%8E%B8%ED%99%94%20%EB%AC%B8%EC%A0%9C%5D%20concat%EC%9D%84%20%EC%9D%B4%EC%9A%A9%ED%95%9C%20%EB%8D%B0%EC%9D%B4%ED%84%B0%20%EB%B3%91%ED%95%A9%20(with%20for%20loop%20clause).ipynb)

---

## List & Dictionary 관련

---

### List 관련

---

### Dictionary 관련

### 두 개의 list를 하나의 Dictionary로 바꾸기

```python
A = ['Apple','Banana','Watermelon']
B = [1, 2, 3]
```

```python
dic = {name : value for name, value in zip(A,B)}
dic
```

```python
# output
{'Apple': 1, 'Banana': 2, 'Watermelon': 3}
```

---

## DataFrame 관련

---

### 1. 컬럼 전처리 관련

### 컬럼명에 접두사 & 접미사 붙이기

```python
df.add_prefix("접두사_")
```

```python
df.add_sufix("_접미사")
```

### 컬럼내의 특정값을 조건문에 따라 변경하고 싶을때

```python
np.where(조건문, True일 경우 변경할 값, False일 경우 변경할 값)
```

```python
# True인 경우만 값을 변경하고 나머지는 값을 유지하고 싶을 때
np.where(조건문, True일 경우 변경할 값, df['유지할 컬럼명'] )
```

---

### 2. 결측치 채우기

### [시계열 데이터의 결측치는 근처값을 채우는게 일반적이다.](https://github.com/gabesoon/Python/blob/main/6.%20Preprocessing/09.%20%5B%EA%B2%B0%EC%B8%A1%EC%B9%98%20%EB%AC%B8%EC%A0%9C%5D%20%EC%8B%9C%EA%B3%84%EC%97%B4%20%EA%B2%B0%EC%B8%A1%EC%B9%98%20%EB%8C%80%EC%B2%B4.ipynb)

---

### 3. ETC.

### DataFrame 저장하는 방법 5가지

csv파일 저장

```python
df.to_csv("파일명.csv")
```

csv 파일 로드

```python
df = pd.read_csv("경로/파일명.csv")
```

Excel 파일로 저장

```python
df.to_excel("파일명.xlsx")
```

Excel 파일 로드

```python
df = pd.read_excel("경로/파일명.xlsx")
```

pickle로 저장하기 (DataFrame외에 list, dict 등 Python의 모든 객체 저장가능)

```python
df.to_pickle("파일명.pkl")
```

pickle 불러오기

```python
df = pd.read_pickle("경로/파일명.pkl")
```

SQLite3 DB로 저장하기

```python
import sqlite3

con = sqlite3.connect("test.db") # 저장할 db선택
df.to_sql("table_name", con, if_exists="append", index=False) # 저장
con.close()
```

SQLite3 DB 불러오기

```python
con = splite3.connect("test.db")
df = pd.read_sql("SELECT * FROM table_name", con) # SQL 쿼리 사용
con.close()
```

df → html 표

```python
df.to_html()
```

html로 저장

```python
df.to_html("test.html")
```

---

### csv 파일을 불러올때 "Unnamed:0" 컬럼을 제외하는 법

1. 저장할때부터 Unnamed:0 이 생성되지 않도록 하기

```python
df.to_csv("파일명", index=False) 
```

2. data를 불러올때 Unnamed:0 을 제외하기

```python
df = pd.read_csv("파일명", index_col = 0 )
```

Resource :  [좋은코딩](https://good-coding.tistory.com/39)

---

<aside>
💡 df중 특정 컬럼 제외하고, 여러개의 컬럼명 동시에 변경하기

</aside>

```python
# 원본 데이터
# col1과 col2를 제외 col3 ~ col8을 변경하고 싶다.

col1   col2   col3   col4   col5   col6   col7   col8
0      5345   rrf    rrf    rrf    rrf    rrf    rrf
1      2527   erfr   erfr   erfr   erfr   erfr   erfr
2      2727   f      f      f      f      f      f
```

```python
# 방법1 
new_names = [(i,i+'_x') for i in df.columns if i not in ['col1','col2']]
```

```python
#방법2 
new_names = [(i,i+'_x') for i in df.iloc[:, 2:].columns.values]
df.rename(columns = dict(new_names), inplace=True)
```

Resource : [Stackoverflow](https://stackoverflow.com/questions/39772896/add-prefix-to-specific-columns-of-dataframe)

## Encoding 관련

### 문자형 데이터를 숫자형 데이터로 바꾸기 : mean_eocoding

<aside>
💡 <장점>
- feature가 이미 너무 많을때 사용하면 좋다. (one_hot encoding만이 능사는 아니다.)
- 데이터의 차원수를 늘리지 않으면서 의미는 도출하고 싶을때!
- mean_encoding의 근간이 되는 feature들은 추후 의미를 역 유추할때 필요하기 때문에 keep 해주는 것이 좋다.
- Regression / Classification 상관없이 예측값에 좀 더 가깝게 학습된다.

<단점>
- 구현과 검증이 쉽지 않다.
- Overfitting 위험이 있다. 
1) Data Leak : train 데이터에 예측에 대한 값이 일부 들어가기 때문에 성능이 올라가는게 어찌보면 당연한 것.
2) 각 Label의 mean값의 출처가 train set 뿐이다 → test set의 Label값의 통계적 분포가 다르면  overfitting이 발생한다.
e.g) Train set의 sex는 male 100 & female 5  <-> Test set의 sex는 male 50 & female 50 인 경우
→ "Train set의 female 5명의 평균 = Test set의 female 50명의 평균" 이라고 보기는 어렵기 때문.

<보완책>
1) Smoothing 기법을 활용해서 train set의 mean을 global mean으로 만들어서 치우쳐진 평균을 보완하는 방법 → Over fitting 방지

2) CV loop 기법을 활용해서 Cross validation 을 통해서 Mean encoding값을 구해서 Label값에 따른 Encoding값을 다양하게 만든다. → Data Leak 방지

</aside>

```python
df = copy.deepcopy(raw_data)

for i in obj_features:
    dynamic_variable = str(i) + '_encode' # 여러개의 feature 동시에 encoding
    globals()[dynamic_variable] = df.groupby(i)['y값'].mean() # 문자열 컬럼 각 인자별 mean값 추출

    new_col = str(i) + '_mean_enc' # 접미사 붙여서 새로운 컬럼 생성
    df.loc[:, new_col] = df[i].map(globals()[dynamic_variable]) # 각 인자별 mean값을 mapping
```

- df.groupby(i)['y값'].mean() 한 값을 list에 담아야 하는데 이를 global로서 대체

Resource : [하나씩 점을 찍어 나가며](https://dailyheumsi.tistory.com/120)

---

## Text data 관련

### Text 데이터 전처리 기본함수

```python
def clean_text(text):
    pattern = '([a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+)' 
    text = re.sub(pattern=pattern, repl='', string=text)
    print("E-mail제거 : " , text , "\n")
    pattern = '(http|ftp|https)://(?:[-\w.]|(?:%[\da-fA-F]{2}))+'
    text = re.sub(pattern=pattern, repl='', string=text)
    print("URL 제거 : ", text , "\n")
    pattern = '([ㄱ-ㅎㅏ-ㅣ]+)'  
    text = re.sub(pattern=pattern, repl='', string=text)
    print("한글 자음 모음 제거 : ", text , "\n")
    pattern = '<[^>]*>'        
    text = re.sub(pattern=pattern, repl='', string=text)
    print("태그 제거 : " , text , "\n")
    pattern = r'\([^)]*\)'
    text = re.sub(pattern=pattern, repl='', string=text)
    print("괄호와 괄호안 글자 제거 :  " , text , "\n")
    pattern = '[^\w\s]'   
    text = re.sub(pattern=pattern, repl='', string=text)
    print("특수기호 제거 : ", text , "\n" )
    text = text.strip()
    print("양 끝 공백 제거 : ", text , "\n" )
    text = " ".join(text.split())
    print("중간에 공백은 1개만 : ", text )
    return text
```

Resource : [All I Need Is Data](https://data-newbie.tistory.com/210)

---

# 2. EDA(Exploratory Data Analysis)

### [코드 1줄로 Data profiling 하기](https://github.com/gabesoon/Data_analysis_Cheatsheet/blob/main/%5BEDA%5D%20Fancy%ED%95%98%EA%B2%8C%20pandas%EB%A1%9C%20EDA%20%ED%95%98%EA%B8%B0(feat.%20Pandas%20Profiling).ipynb)

---

# 3. Visualization

---

# 4. Modeling

---

## [코드 2줄로 30초만에 수십개의 모델 성능 테스트가 가능하다?!](https://github.com/gabesoon/Data_analysis_Cheatsheet/blob/main/%5BModeling%5D%20%EC%BD%94%EB%93%9C%202%EC%A4%84%EB%A1%9C%2010%EC%B4%88%EB%A7%8C%EC%97%90%20%EC%88%98%EC%8B%AD%EA%B0%9C%EC%9D%98%20%EB%AA%A8%EB%8D%B8%EC%84%B1%EB%8A%A5%20%EC%B8%A1%EC%A0%95%ED%95%98%EA%B8%B0.ipynb)

## 학습용 Fake 데이터를 만들기

<aside>
💡 fake text, fake credit card number 등을 생성할 수 있다.
자세한 내용은 Official Document를 확인

</aside>

```python
# faker 설치
!pip install faker
```

```python
from faker import Faker
fake = Faker()

print(fake.name(),'\n')
print(fake.address(),'\n')
print(fake.text(),'\n')
print(fake.credit_card_number(),'\n')
print(fake.profile())
```

```python
Deanna Davidson 

73742 Mason Views Apt. 888
Port Jennifer, VA 06823 

Task campaign article special then modern senior. Dinner table during both moment me. Cold establish behavior war power along general.
World focus long and knowledge. 

6517880058325992 

{'job': 'Clothing/textile technologist', 'company': 'Pham LLC', 'ssn': '726-76-1858', 'residence': '225 Penny Ports Suite 467\nPort Sarah, AZ 26632', 'current_location': (Decimal('0.4203825'), Decimal('87.997714')), 'blood_group': 'A-', 'website': ['https://thomas-macias.com/', 'https://www.parrish-lee.biz/', 'http://www.graham-leonard.org/'], 'username': 'davidmiller', 'name': 'Debbie Wright', 'sex': 'F', 'address': '8629 Robert Brooks\nRossville, MN 77897', 'mail': 'tuckerrobyn@yahoo.com', 'birthdate': datetime.date(1906, 3, 15)}
```

Resource : [Faker Official Document](https://faker.readthedocs.io/en/master/)

---

---

# 5. Etc

---

## Jupyter 에서 long-running cell이 완료되었을때 알림 받기

<aside>
💡 → 작업이 완료될 경우 브라우져의 pop up 알림이 뜬다.

</aside>

```python
#!pip install jupyternotify

%%notify
import time
for seconds in range(1,5):
		print("Working on {} seconds...".format(seconds))
		time.sleep(seconds)
```

---

## pip 특정 버전 설치 & upgrdae

```python
# 특정 버전 설치
pip install package_name==package version
```

```python
# 특정 패키지 업데이트
pip install --upgrade package_name
```

```python
# 특정 패키지를 특정 버전으로 upgrade
pip install --upgrade package_name==package version
```

[Resource: 삵 izz well](https://gentlesark.tistory.com/26)

---