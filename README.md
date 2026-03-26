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

const PORT = process.env.PORT || 3000;

app.listen(PORT, () => {
  console.log("Servidor rodando na porta " + PORT);
});
