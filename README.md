# Projeto de Conclusão de Automação de Testes com CI/CD (GitHub Actions)

Este repositório contém a solução do trabalho prático da pós-graduação em Automação de Testes. O objetivo é implementar uma esteira de Integração Contínua (CI) utilizando GitHub Actions.

## 🚀 Conceitos Utilizados

* **Integração Contínua (CI):** Prática de desenvolvimento onde as alterações de código são integradas e testadas automaticamente de forma frequente, detectando erros o mais rápido possível.
* **GitHub Actions:** Ferramenta integrada ao GitHub que permite automatizar fluxos de trabalho (workflows) diretamente no repositório.
* **Workflows, Jobs e Steps:** 
    * *Workflow:* O processo automatizado completo.
    * *Job:* Conjunto de etapas que executam em uma mesma máquina virtual.
    * *Steps:* Tarefas individuais executadas em sequência (comandos ou Actions prontas).
* **Artefatos (Artifacts):** Arquivos gerados durante a execução (como relatórios) que são salvos pelo GitHub para download posterior.

---

## ⚙️ Gatilhos da Pipeline

A pipeline foi configurada para atender aos três gatilhos obrigatórios:
1. **Push:** Executa automaticamente a cada atualização nas branches `main` ou `master`.
2. **Manual (`workflow_dispatch`):** Permite executar os testes manualmente pela aba "Actions" do GitHub.
3. **Agendada (`schedule / cron`):** Configurada para rodar de forma periódica automaticamente.

---

## 📊 Relatórios de Testes

Os relatórios são gerados após a execução dos testes. A pipeline utiliza a condição `if: always()` para garantir que o relatório seja salvo como um **Artefato** na pipeline mesmo se algum teste falhar, permitindo a análise dos resultados.
