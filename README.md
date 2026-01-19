# Athos Sperber — Engenheiro de Software (Arquitetura, Governança e Sistemas)

Desenvolvedor com foco em **arquitetura de sistemas**, **governança**, **rastreabilidade** e integração **plataforma → produto**.  
Curto construir soluções com **contratos claros**, demos reproduzíveis e evolução controlada (sem “feature Frankenstein”).

<div>
  <img alt="Python" src="https://img.shields.io/badge/Python-1C1C1C?style=for-the-badge&logo=python&logoColor=FFD700" />
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-1C1C1C?style=for-the-badge&logo=typescript&logoColor=FFD700" />
  <img alt="React" src="https://img.shields.io/badge/React-1C1C1C?style=for-the-badge&logo=react&logoColor=FFD700" />
  <img alt="AWS" src="https://img.shields.io/badge/AWS-1C1C1C?style=for-the-badge&logo=amazonaws&logoColor=FFD700" />
  <img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub_Actions-1C1C1C?style=for-the-badge&logo=githubactions&logoColor=FFD700" />
</div>

---

## 🔥 Projetos âncora

### 🚦 governanca-system (framework)
Framework de governança com fluxo **Task → Action → Report**, rastreabilidade por eventos (**append-only**) e separação explícita: **histórico ≠ simulação**.

- Repo: https://github.com/AthosSperber/governanca-system  
- Demo (GitHub Pages): https://athossperber.github.io/governanca-system/  
- Snapshot governado (JSON): https://athossperber.github.io/governanca-system/governed_snapshot_conexao_solar.json  

---

### 🌞 ConexaoSolar (produto React/TS)
Landing/produto **mobile-first** para consultores, com **Painel do Consultor** consumindo artefatos governados (sem backend).

- Repo: https://github.com/AthosSperber/ConexaoSolar  
- Deploy: https://conexao-solar.vercel.app  
- Rota consultor: `/para-consultores`

---

## ☁️ Projeto AWS (em andamento) — Artefatos Assinados
Objetivo: elevar os artefatos governados para um nível de **integridade verificável**.

**Ideia:** publicar snapshots em **S3 + CloudFront** e gerar assinatura criptográfica (hash + assinatura) via pipeline (GitHub Actions).  
Assim, o consumidor (frontend) consegue provar que o JSON **não foi alterado** entre a geração e o consumo.

**Componentes planejados:**
- S3 (armazenamento dos artefatos)
- CloudFront (distribuição/CDN)
- KMS (assinatura/gestão de chaves) *ou* assinatura gerada no pipeline com chave protegida
- GitHub Actions (build + publish)

**Entrega MVP:**
- `snapshot.json`
- `snapshot.json.sha256`
- `snapshot.json.sig`
- Documentação de verificação (CLI)

> Status: roadmap / construção (vou evoluir e publicar o repositório dedicado).

---

## 📫 Contato
- LinkedIn: https://www.linkedin.com/in/athos-sperber

---

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=AthosSperber&theme=transparent&show_icons=true&hide_title=true&border_radius=16)
