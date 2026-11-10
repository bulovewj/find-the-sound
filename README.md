# find-the-sound · 계이름 악보 변환기

리코더나 노래 한 줄을 녹음하거나 올리면 음정을 찾아 오선 악보로 그리고, 음표 아래에 계이름(고정도법)을 달아 주는 웹 페이지입니다.

- 음정 인식: [Spotify Basic Pitch](https://github.com/spotify/basic-pitch-ts) (Apache-2.0), 브라우저 안에서 TF.js로 실행
- 악보: [abcjs](https://github.com/paulrosen/abcjs) · MIDI: [@tonejs/midi](https://github.com/Tonejs/Midi) · PDF: [jsPDF](https://github.com/parallax/jsPDF)
- 서버 없음. 음원은 브라우저 밖으로 나가지 않습니다.

## 기능
1. 음원 올리기(mp3·wav·m4a) 또는 🎤 마이크로 녹음(최대 30초)
2. 악보로 바꾸기 → 조성·박자·빠르기 추정
3. 조 바꾸기(다·바·사·라·내림나장조), 리코더 쉬운 조 추천
4. 음표 눌러 고치기(↑↓ 반음, Delete 지우기, 되돌리기)
5. 원본/악보 듣기, PDF·MIDI·ABC 내려받기

`model/`의 Basic Pitch 가중치는 원본 `group1-shard1of1.bin`을 base64 텍스트로 바꾼 것입니다.
