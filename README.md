# BIG

# 정규 표현식이란
문자열에서 특정 내용을 찾거나 대체 또는 발췌하는데 사용되는 식이다.
반복문과 조건문을 사용해야 할 복잡한 코드들을 정규 표현식으로 이용하면 매우 간단하게 표현될 수 있기에 필요하다.

정규 표현식 구성코드는 슬래쉬 문자 두개 사이로 정규식 기호가 들어가는 형태이다.
EX) /regexr/i   (뒤에 i는 정규식 플래그)






# 정규 표현식 코드

문자열에서 패턴 검색하기 (re.search() 사용) 
import re


string = "Hello, World!"
pattern = r"Hello"
match = re.search(pattern, string)
if match:
print("일치하는 패턴을 찾았습니다:", match.group())
else:
print("일치하는 패턴이 없습니다.")

문자열에서 패턴 일치하는 모든 항목 찾기 (re.findall() 사용) 
import re


string = "apple, banana, cherry, date"
pattern = r"\b\w+\b"  # 단어 경계로 구분된 단어들
matches = re.findall(pattern, string)
print("일치하는 패턴들:", matches)

문자열에서 패턴 일치하는 항목 치환하기 (re.sub() 사용) 
import re


string = "Hello, World!"
pattern = r"World"
replacement = "Python"
new_string = re.sub(pattern, replacement, string)
print("치환된 문자열:", new_string)

문자열 분할하기 (re.split() 사용) 
import re


string = "apple,banana,cherry,date"
pattern = r","
parts = re.split(pattern, string)
print("분할된 문자열:", parts)
