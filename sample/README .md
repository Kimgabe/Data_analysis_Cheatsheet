# README

# Data_analysis_Cheatsheet

## Preprocessing

---

1. [서로 길이가 다른 list/Series를 DataFrame으로 만들기](https://github.com/gabesoon/Data_analysis_Cheatsheet/blob/main/%5BProprocessing%5D%20%EC%84%9C%EB%A1%9C%20%EA%B8%B8%EC%9D%B4%EA%B0%80%20%EB%8B%A4%EB%A5%B8%20list%20or%20Series%20%EC%97%AC%EB%9F%AC%EA%B0%9C%EB%A5%BC%20%ED%95%A9%EC%B3%90%EC%84%9C%20DataFrame%20%EB%A7%8C%EB%93%A4%EA%B8%B0.ipynb)

---

## Etc

---

1. csv 파일을 불러올때 "Unnamed:0" 컬럼을 제외하는 법

```python
# 1. 저장할때부터 Unnamed:0 이 생성되지 않도록 하기
df.to_csv("파일명", index=False) 

# 2. data를 불러올때 Unnamed:0을 제외하기
df = pd.read_csv("파일명", index_col = 0 )
```