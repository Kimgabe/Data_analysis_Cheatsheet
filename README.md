# README

# Data_analysis_Cheatsheet

## Preprocessing

---

1. [서로 길이가 다른 list/Series를 DataFrame으로 만들기](https://github.com/gabesoon/Data_analysis_Cheatsheet/blob/main/%5BProprocessing%5D%20%EC%84%9C%EB%A1%9C%20%EA%B8%B8%EC%9D%B4%EA%B0%80%20%EB%8B%A4%EB%A5%B8%20list%20or%20Series%20%EC%97%AC%EB%9F%AC%EA%B0%9C%EB%A5%BC%20%ED%95%A9%EC%B3%90%EC%84%9C%20DataFrame%20%EB%A7%8C%EB%93%A4%EA%B8%B0.ipynb)
2. [Pandas String 데이터 기본 전처리](https://github.com/gabesoon/Data_analysis_Cheatsheet/blob/main/%5BProprocessing%5D%20Pandas%20String%20%EB%8D%B0%EC%9D%B4%ED%84%B0%20%EA%B8%B0%EB%B3%B8%20%EC%A0%84%EC%B2%98%EB%A6%AC.ipynb)
    - 
        
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
        
3. Merge 관련
    - 
        
        [시간과 날짜 컬럼 데이터의 병합은 'apply'를 써야 한다.](https://github.com/gabesoon/Python/blob/main/6.%20Preprocessing/03.%20%5B%EB%8D%B0%EC%9D%B4%ED%84%B0%20%ED%8C%8C%ED%8E%B8%ED%99%94%20%EB%AC%B8%EC%A0%9C%5D%20%20%ED%8F%AC%EB%A7%B7%EC%9D%B4%20%EB%8B%A4%EB%A5%B8%20%EB%8D%B0%EC%9D%B4%ED%84%B0%20%EB%B3%91%ED%95%A9(merge)_(1)%20%EC%B0%B8%EC%A1%B0%20%EB%8D%B0%EC%9D%B4%ED%84%B0%EA%B0%80%20%ED%95%84%EC%9A%94%EC%97%86%EB%8A%94%20%EA%B2%BD%EC%9A%B0.ipynb)
        
        [일정한 패턴이 없거나, 포맷이 다른 데이터 병합은 참고자료를 쓴다.](https://github.com/gabesoon/Python/blob/main/6.%20Preprocessing/04.%20%5B%EB%8D%B0%EC%9D%B4%ED%84%B0%20%ED%8C%8C%ED%8E%B8%ED%99%94%20%EB%AC%B8%EC%A0%9C%5D%20%20%ED%8F%AC%EB%A7%B7%EC%9D%B4%20%EB%8B%A4%EB%A5%B8%20%EB%8D%B0%EC%9D%B4%ED%84%B0%20%EB%B3%91%ED%95%A9(merge)_(2)%20%EC%B0%B8%EC%A1%B0%20%EB%8D%B0%EC%9D%B4%ED%84%B0%EA%B0%80%20%ED%95%84%EC%9A%94%ED%95%9C%20%EA%B2%BD%EC%9A%B0.ipynb)
        
4. DataFrame 관련
    - 
        
        컬럼명에 접두사를 붙일때
        
        ```python
        df.add_prefix("접두사_")
        ```
        
        컬럼명에 접미사를 붙일때
        
        ```python
        df.add_sufix("_접미사")
        ```
        
5. 결측치 채우기
    - 
        
        [시계열 데이터의 결측치는 근처값을 채우는게 일반적이다.](https://github.com/gabesoon/Python/blob/main/6.%20Preprocessing/09.%20%5B%EA%B2%B0%EC%B8%A1%EC%B9%98%20%EB%AC%B8%EC%A0%9C%5D%20%EC%8B%9C%EA%B3%84%EC%97%B4%20%EA%B2%B0%EC%B8%A1%EC%B9%98%20%EB%8C%80%EC%B2%B4.ipynb)
        

---

## Etc

---

<aside>
💡 1. csv 파일을 불러올때 "Unnamed:0" 컬럼을 제외하는 법

</aside>

- 펼치기
    
    1. 저장할때부터 Unnamed:0 이 생성되지 않도록 하기
    
    ```python
    df.to_csv("파일명", index=False) 
    ```
    
    2. data를 불러올때 Unnamed:0 을 제외하기
    
    ```python
    df = pd.read_csv("파일명", index_col = 0 )
    ```
    
    출처 :  [좋은코딩](https://good-coding.tistory.com/39)