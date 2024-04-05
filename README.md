# hwp
Запрос: https://api.nasa.gov/planetary/apod?api_key=jUsYymkf0vV58o8oJUSsls07GhfVpBW1HmURrBla&date=2024-05-05
Что случилось: {"code":400,"msg":"Date must be between Jun 16, 1995 and Apr 05, 2024.","service_version":"v1"}
Вывод: Задан нейдействительный параметр
Код: 
import requests

def test_status_code_200():
    date = "2024-05-05"
    url = f"https://api.nasa.gov/planetary/apod?api_key=jUsYymkf0vV58o8oJUSsls07GhfVpBW1HmURrBla&date={date}"
    response = requests.get(url)
    result = response.status_code
    assert 200 <= result < 400, f"Expected status code 2xx, but got {result}"
