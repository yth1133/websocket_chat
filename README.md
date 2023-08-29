# websocket_chat 사용법 정리

pip install fastapi<br>
pip install uvicorn<br>
pip install websockets<br>
pip install jinja2<br>

기본 웹소켓 실행은 터미널에서<br>
uvicorn websocket_chat:app --reload <br>
브라우저에서 http://127.0.0.1:8000 접속하면 됩니다.


### 같은 와이파이에서 다른 기기에서 접속하는 방법 정리 ### <br>

ws_chat.html 파일의  
var ws = new WebSocket("ws://localhost:8000/chatting");  
이부분을  
var ws = new WebSocket("ws://서버의ip주소:8000/chatting");  
로 바꾸시면 됩니다.  
그리고 uvicorn websocket_chat:app --reload --host 0.0.0.0  으로 실행해주세요  

서버의 ip주소는 cmd 창에서 ipconfig 했을 시에 IPv4 주소가 본인의 ip 주소입니다.  
