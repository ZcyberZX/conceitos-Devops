from fastapi import FastAPI

app = FastAPI()

# Rota raiz
@app.get("/")
def read_root():
    return {"mensagem": "API de exemplo para CI/CD"}

# Rota de saudação
@app.get("/saudacao/{nome}")
def saudacao(nome: str):
    return {"mensagem": f"Olá, {nome}! Bem-vindo à API de CI/CD 🚀"}

# Rota de status
@app.get("/status")
def status():
    return {"status": "online", "versao": "1.0.0"}

