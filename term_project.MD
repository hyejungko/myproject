#기말프로젝트계획서

import requests
resp = requests.get("https://finance.naver.com/marketindex/")
resp.raise_for_status()
resp.encoding = None

이하 구상중
구체적으로는 requests를 통해 네이버 증권 사이트에서 나라별 환율을 뽑아내는
프로그램을 진행하고자 합니다. https://finance.naver.com/marketindex/에 공시되어 있는
미국 USD 일본 JPY 유럽연합 EUR 중국 CNY 를 중심으로 환율을 알아보고자 합니다.
한글이 깨지는 문제를 해결하기 위해 (인코딩 문제) 미리 EUC-KR이나 NONE으로 지정하고 
원하는 택스트의 속성을 읽어내는 과정을 거치려고 합니다.
