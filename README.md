
## Como executar esse projeto?

* Rodar o Jaeger em container
* Clone esse repositório.
* Crie um virtualenv com Python 3.
* Ative o virtualenv.
* Instale as dependências.
* Rode o App.

```
docker run -d -p6831:6831/udp -p16686:16686 jaegertracing/all-in-one:latest
git clone https://github.com/leandro-matos/jaeger-example
cd jaeger-example
python3 -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python movie-jaeger.py <movie>
```

Acessar o endereço http://localhost:16686/ para consultar todas as métricas geradas e fazer o tracing da aplicação