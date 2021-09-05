2021.09.05

------

- HTML 연습문제
- 이번주에 들은 HTML 강의 내용 연습문제

##### 느낀점

- 대부분의 문제는 금방 풀었다.
- 문제 4) 아직까지 table에 대한 태그가 조금 헷갈려서 더듬더듬 만들었다. 좀 더 만드는 연습을 할 필요가 있는듯..!
- 문제 5) &#8747; `&#8747;` 아주 생소한 특수문자..? 구글의 도움을 받아야했다. ㅎㅎ 문자만 나열하면 문제 예시와는 달리 붙어서 출력되는 것이 있어서 공백`&nbsp;`을 사용했다.
- 모범답안이 나오면 비교해볼것!

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>문제1)</p>
    <div class="1">
        <h1>다람쥐 헌 쳇바튀에 타고파</h1>
        <h2>다람쥐 헌 쳇바튀에 타고파</h2>
        <h3>다람쥐 헌 쳇바튀에 타고파</h3>
        <h4>다람쥐 헌 쳇바튀에 타고파</h4>
        <h5>다람쥐 헌 쳇바튀에 타고파</h5>
        <h6>다람쥐 헌 쳇바튀에 타고파</h6>
    </div>

    <br>

    <p>문제2)</p>
    <div class="2">
        <ul>
            <li>사과</li>
            <li>오렌지</li>
            <li>포도</li>
            <li>체리</li>
        </ul>

        <ol>
            <li>가지</li>
            <li>감자</li>
            <li>당근</li>
            <li>대파</li>
        </ol>
    </div>

    <br>

    <p>문제3)</p>
    <div class="3">
        <input type="password" 
        title="password" 
        minlength="6" 
        maxlength="20"
        placeholder="비밀번호를 입력해주세요">
    </div>

    <br>
    
    <p>문제4)</p>
    <div class="4">
        <table border="1">
            <caption><h2>주식회사 HTML 매출</h2></caption>
            <thead>
                <tr>
                    <th rowspan="2">/</th>
                    <th colspan="2">반기</th>
                    <th rowspan="2">합계</th>
                    <th rowspan="2">비고</th>
                </tr>
                <tr>
                    <th>전반기</th>
                    <th>후반기</th>
                </tr>
                <tbody>
                    <tr>
                        <th>2019</th>
                        <td>10억</td>
                        <td>20억</td>
                        <td>30억</td>
                        <td></td>
                    </tr>
                    <tr>
                        <th>2020</th>
                        <td>22억</td>
                        <td>33억</td>
                        <td>55억</td>
                        <td rowspan="2">1)</td>
                    </tr>
                    <tr>
                        <th>2021</th>
                        <td colspan="2">집계중</td>
                        <td>집계중</td>
                    </tr>
                </tbody>
        </table>
    </div>

    <br>

    <p>문제5)</p>
    <div class="5">
        <p><i>&#8747;</i><sub>0</sub><sup><i>t&nbsp;</i></sup>2<sup>5</sup>x<i>log</i><sub>2</sub>x</p>
    </div>
</body>
</html>

```

