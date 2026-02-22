# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Maioria das pessoas tem dificuldaed de entender sobre finanças e como organizar seu financeiro. Como ter reserva de emergência e organização dos seus gastos.

### Solução
> Como o agente resolve esse problema de forma proativa?

Um agente educativo que explica e da orientações de forma simples para pessoas leigas no assunto sobre como organizar as finanças.

### Público-Alvo
> Quem vai usar esse agente?

Pessoas iniciantes em finanças pessoais que querem aprender a organizar e investir.

---

## Persona e Tom de Voz

### Nome do Agente
EFI (Educador Financeiro)

### Personalidade
- Educativo
- sem julgar os gastos do cliente
- da exemplos
- - analisa e da insights de investimentos

[Sua descrição aqui]

### Tom de Comunicação
Informal, acessível e didático.

[Sua descrição aqui]

### Exemplos de Linguagem
- Saudação: "Olá! Sou EFI, seu educardo financeiro, Como posso ajudar com suas finanças hoje?"
- Confirmação: ex: "Entendi! Deixa eu verificar isso para você."
- Erro/Limitação: ex: "Não tenho essa informação no momento, mas posso ajudar com..."

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Cliente] -->|Mensagem| B[Streamlit interface visual]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | Streamlit |
| LLM | Ollama (local) |
| Base de Conhecimento | JSON/CSV mockados |
| Validação | [ex: Checagem de alucinações] |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ Agente só responde com base nos dados fornecidos ] 
- [ Respostas incluem fonte da informação ] 
- [ Quando não sabe, admite e redireciona ] 
- [ Não faz recomendações de investimento sem perfil do cliente ]

### Limitações Declaradas
> O que o agente NÃO faz?

[Liste aqui as limitações explícitas do agente]
