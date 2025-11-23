user vvv 488
------------------
Пробовал на буке света

--------------------
Проба на XeonPC
Oracle Virtual box - Linux O 64
M:\Downloads\HA
первый запуск - долго
new bak 
+ File editor
+ Piper
+ Whisper - run долго - errs out of memory
-----
re from bak
new VM ha07 - mem2 cpu2

https://psenyukov.ru/управление-голосом-умным-домом-home-assistant-с-по/
setup Whisper ... + - config tiny8 ru 1 - run ... +  wait 1m - Whisper Wyoming Protocol add - 
    Assist - ru ru ru - error опять!
    Need language stt_language for stt_engine stt.faster_whisper. Got 
```json
    {'name': 'Home Assistant', 'language': 'ru', 'conversation_engine': 'conversation.home_assistant', 'conversation_language': 'ru', 'prefer_local_intents': False, 'stt_engine': 'stt.faster_whisper', 'stt_language': None, 'tts_engine': None, 'tts_language': None, 'tts_voice': None, 'wake_word_entity': None, 'wake_word_id': None}
```
    https://github.com/home-assistant/core/issues/156705
  + File editor
  непомогло
  выбирая en - рус получилось


+ Piper - config - run

ass -  "какая погода" - не предоставлен - дал
"погода" письменно - ответилнаписал - по голосу - написалОтветил
Piper - add Wyoming Protocol
---------
в app на телефоне на голос "погода" отвечает голосом - ок
    добавлять Альт название "погода" не обязательно
---------

