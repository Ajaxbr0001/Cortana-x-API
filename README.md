# Cortana-x-API
Cortana 
import express from "express";

const app = express();
app.use(express.json());

app.get("/", (req, res) => {
  res.send("API da Cortana X online 🚀");
});

app.post("/chat", async (req, res) => {
  const mensagem = req.body.mensagem;

  const respostaFake = "Você disse: " + mensagem;

  res.json({ resposta: respostaFake });
});

app.listen(3000, () => {
  console.log("Servidor rodando na porta 3000");
});
