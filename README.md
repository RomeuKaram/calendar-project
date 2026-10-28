# 📅 Calendário Regressivo Escolar 2026

> Contagem regressiva inteligente até as férias escolares — com distinção entre dias corridos e dias letivos.

[GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen?style=for-the-badge)
[HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
[CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
[JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
[License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

🔗 **Acesse ao vivo:** https://romeukaram.github.io/calendar-project/

---

### 🎯 Preview

```
[Dias corridos para as férias]  51|13|15|11  DD | HH | MM | SS
[Dias letivos para as férias]    35|13|15|11  Fins de semana e feriados não consomem tempo

OUTUBRO 2026 | NOVEMBRO 2026 | DEZEMBRO 2026
[Calendário mensal com contagem por dia]
```

> O print acima é do projeto rodando em 28/10/2026. Cada dia mostra `faltam X dias`, feriados, fins de semana e dias concluídos.

---

### ✨ O que faz

Este não é um calendário comum. Ele resolve um problema real de professores e alunos: **quanto tempo falta DE VERDADE**.

- **Duas contagens simultâneas:**
  - `Dias corridos`: tempo real até 18/12/2026 às 22:00
  - `Dias letivos`: desconta fins de semana e feriados — o relógio "congela" fora do horário escolar
- **Calendário visual de Outubro a Dezembro 2026**
  - Mostra quantos dias faltam em cada data futura
  - Marca automaticamente: Hoje, Concluído, Fim de semana, Feriado, Férias 🎉
- **100% responsivo e offline**
  - Sem frameworks, sem build — HTML + CSS + JS puro
  - Atualização automática a cada segundo

### 🧠 Diferencial técnico

A lógica `schoolTimeUntil()` é o coração do projeto:

```js
function schoolTimeUntil(target, current) {
  // Avança dia a dia até o alvo
  // Só soma milissegundos se isSchoolDay(cursor)
  // Fim de semana e feriado não consomem tempo
}
```

Isso garante que a contagem de dias letivos seja precisa, mesmo com feriados prolongados como 12/10, 02/11, 15/11 e 20/11.

### 🎨 Refinamentos (v2.0)

Corrigidos nesta versão:

- **Alinhamento no cantinho:** `day-number` e `day-status` agora começam no canto superior esquerdo (`display:flex; align-items:flex-start; text-align:left`) para melhor aproveitamento de espaço
- **Fix de overflow de feriados:** `holiday-name` com `-webkit-line-clamp: 3; word-break: break-word;` evita vazamento de nomes grandes como "Nossa Senhora Aparecida" e "Proclamação da República"
- **Legibilidade:** status com `0.62rem` e peso 600, truncamento inteligente

### 📁 Estrutura

```
calendar-project/
├── index.html        # arquivo único, pronto para GitHub Pages
└── README.md         # este arquivo
```

### 🚀 Como usar

1. Clone:
```bash
git clone https://github.com/romeukaram/calendar-project.git
```
2. Abra `index.html` ou acesse via Pages
3. Para testar outra data, edite:
```js
const TEST_NOW = "2026-11-10T08:00:00"; // ou null para usar data real
```

### 🗓️ Feriados configurados 2026

```js
"2026-10-12": "Nossa Senhora Aparecida",
"2026-11-02": "Finados",
"2026-11-15": "Proclamação da República",
"2026-11-20": "Consciência Negra"
```

### 🛠️ Tecnologias

- HTML5 semântico
- CSS Grid + Flexbox
- JavaScript puro (Date API, sem libs)

### 👨‍🏫 Autor

**Prof. Romeu Karam**  
Maringá - PR | [Instagram @romeukaramneto](https://instagram.com/romeukaramneto) | [GitHub](https://github.com/romeukaram)

> Projeto educacional criado para auxiliar no planejamento do 4º bimestre.

### 📄 Licença

MIT - use livremente em sua escola.

---

### 🔜 Próximos passos

- [ ] Edição Especial Colégio Estadual Visconde de Guarapuava (com identidade CEVG)
- [ ] Seletor de ano letivo
- [ ] Exportar para Google Calendar
