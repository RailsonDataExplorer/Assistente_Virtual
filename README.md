# 🤖 Assistente Virtual com Reconhecimento de Voz e Automações 🚀

Este projeto implementa um **Assistente Virtual** capaz de processar comandos de voz, realizar pesquisas no Wikipedia, abrir o YouTube, encontrar farmácias próximas e muito mais. Ele utiliza bibliotecas como `SpeechRecognition`, `gTTS`, `wikipedia-api`, `geopy` e `pydub` para proporcionar uma experiência interativa e funcional.

---

## 📋 Índice

- [🔧 Funcionalidades](#funcionalidades)
- [💻 Requisitos](#requisitos)
- [🔧 Instalação](#instalação)
- [🚀 Uso](#uso)
- [📂 Estrutura do Projeto](#estrutura-do-projeto)
- [📝 Notas Técnicas](#notas-técnicas)
- [📜 Licença](#licença)
- [🙏 Reconhecimentos](#reconhecimentos)
- [🌐 Links Úteis](#links-úteis)

---

## 🔧 Funcionalidades

- **🎤 Speech-to-Text**: Converte áudio capturado em texto.
- **📢 Text-to-Speech**: Converte texto em áudio para comunicação com o usuário.
- **📚 Pesquisa no Wikipedia**: Realiza pesquisas rápidas no Wikipedia.
- **📺 Abrir YouTube**: Gera links diretos para o YouTube.
- **🏥 Encontrar Farmácia Próxima**: Utiliza coordenadas geográficas para localizar farmácias próximas via Google Maps.
- **🔄 Conversão de Áudio**: Converte arquivos de áudio para o formato `.wav` antes do processamento.

---

## 💻 Requisitos

- **Google Colab** (ou ambiente Python com suporte a bibliotecas de áudio).
- Bibliotecas:
  - [`SpeechRecognition`](https://pypi.org/project/SpeechRecognition/)
  - [`gTTS`](https://github.com/pndurette/gTTS)
  - [`wikipedia-api`](https://wikipedia-api.readthedocs.io/en/latest/)
  - [`geopy`](https://geopy.readthedocs.io/en/stable/)
  - [`pywhatkit`](https://pypi.org/project/pywhatkit/)
  - [`pydub`](https://pydub.com/)
  - [`ffmpeg`](https://ffmpeg.org/)

---

## 🔧 Instalação

1. **Instalar Dependências**
   ```bash
   !pip install SpeechRecognition gTTS wikipedia-api geopy pywhatkit pydub ffmpeg
   ```
2. **Importar Bibliotecas**

```bash
import speech_recognition as sr
from gtts import gTTS
import os
import wikipediaapi
from geopy.geocoders import Nominatim
from geopy.distance import geodesic
from IPython.display import Audio
from pydub import AudioSegment
from google.colab import files
```
## 🚀 Uso
1. **Inicializar o Assistente Virtual**
Execute o código principal para iniciar o assistente:
```bash
virtual_assistant()
```
2. **Comandos Suportados**
Pesquisar no Wikipedia : Diga algo como "Pesquisar Python".
Abrir YouTube : Diga "Abrir YouTube".
Encontrar Farmácia Próxima : Diga "Encontrar farmácia".
Sair : Diga "Sair" para encerrar o assistente.
3. **Upload de Áudio**
Grave um áudio localmente (por exemplo, dizendo "Pesquisar Python").
Salve o áudio em qualquer formato suportado (.wav, .opus, .mp3, etc.).
Faça upload do arquivo no Google Colab quando solicitado pelo assistente.
## 📂 Estrutura do Projeto
```bash
/content/
├── virtual_assistant_project/       # Pasta principal do projeto
│   ├── main.ipynb                    # Notebook principal
│   ├── requirements.txt              # Lista de dependências
│   ├── audio_files/                  # Pasta para armazenar arquivos de áudio
│   │   ├── input/                    # Arquivos de entrada para processamento
│   │   └── output/                   # Arquivos convertidos (.wav)
│   ├── utils/                        # Funções utilitárias
│   │   ├── speech_to_text.py         # Funções para reconhecimento de fala
│   │   ├── text_to_speech.py         # Funções para conversão de texto em áudio
│   │   ├── wikipedia_search.py       # Funções para pesquisa no Wikipedia
│   │   ├── location_services.py      # Funções para localização geográfica
│   │   └── audio_conversion.py       # Funções para conversão de áudio
└── README.md                         # Documentação do projeto
```
## 📝 Notas Técnicas
**🎤 Speech-to-Text** : Usa a API do Google (recognize_google) para converter áudio em texto.
**📢 Text-to-Speech** : Utiliza a biblioteca gTTS para gerar áudio a partir de texto.
**🌍 Localização Geográfica** : Usa geopy para obter coordenadas e calcular distâncias.
**🔗 URLs Dinâmicos** : Gera links para o YouTube e Google Maps para navegação direta.
**🔄 Conversão de Áudio** : Usa pydub e ffmpeg para converter arquivos de áudio para .wav.
## 📜 Licença
Este projeto é distribuído sob a licença MIT. Para mais detalhes, consulte o arquivo LICENSE .

## 🙏 Reconhecimentos
SpeechRecognition : Biblioteca para reconhecimento de fala.
gTTS : Ferramenta para conversão de texto em áudio.
Wikipedia-API : Interface para acessar o Wikipedia.
Geopy : Biblioteca para localização geográfica.
PyDub & FFmpeg : Ferramentas para manipulação de áudio.
## 🌐 Links Úteis

- **📚 Documentação do SpeechRecognition**: [https://pypi.org/project/SpeechRecognition/](https://pypi.org/project/SpeechRecognition/)
- **🔗 Repositório gTTS no GitHub**: [https://github.com/pndurette/gTTS](https://github.com/pndurette/gTTS)
- **📄 Paper Wikipedia-API**: [https://wikipedia-api.readthedocs.io/en/latest/](https://wikipedia-api.readthedocs.io/en/latest/)
- **🎓 Tutorial Google Colab**: [https://colab.research.google.com/](https://colab.research.google.com/)
- **🔗 PyDub Documentation**: [https://pydub.com/](https://pydub.com/)
