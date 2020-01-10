# Indonesia Sentiment Analyzer API

Analisa dan Dapatkan sentiment dari text berbahasa indonesia dengan alat ini

## Install

1. proyek ini di test dan dibuat menggunakan python3
2. `pip3 install -r requirements.txt --user`
4. jalankan `python3 serve.py` pada direktori proyek

## Usage

Lakukan `POST` ke route `/` dengan parameter `text`

Contoh POST Request : 

```bash
curl -F "text=halo apa kabar" http://localhost:8000
```

```
POST  HTTP/1.1
Host: localhost:8000?text=halo apa kabar, aku senang bertemu dengan kamu
cache-control: no-cache
```

Contoh Response : 

```
{
    "classified_text": "halo apa kabar, aku senang [4] bertemu dengan kamu",
    "original_text": " halo apa kabar, aku senang bertemu dengan kamu",
    "sentence_score": [
        "halo apa kabar, aku senang [4] bertemu dengan kamu"
    ],
    "max_positive": 4,
    "max_negative": -1,
    "kelas": "positive"
}
```

## Credits

- This project are exapanded from [https://github.com/masdevid/sentistrength_id.git](https://github.com/masdevid/sentistrength_id.git)