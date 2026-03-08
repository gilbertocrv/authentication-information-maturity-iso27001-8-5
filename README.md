# ISO/IEC 27001:2022 – Controle 8.5: Secure Authentication

## 🎯 Objetivo
Este repositório contém a ferramenta de avaliação de maturidade para o Controle 8.5 da ISO 27001:2022. O foco é medir a robustez dos mecanismos de autenticação, indo além da simples senha e explorando conceitos de **Zero Trust** e **Autenticação Adaptativa**.

## 🧩 Grupos de Controle Avaliados
A ferramenta divide o Controle 8.5 em quatro domínios críticos:
1. **MFA (Multifator):** Garantia de fatores de naturezas distintas (Conhecimento, Posse, Inerência).
2. **RBA & Step-Up:** Inteligência contextual para elevar o nível de autenticação em ações críticas.
3. **Resiliência contra Ataques:** Defesas contra Brute Force, Credential Stuffing e Session Hijacking.
4. **Governança de Logs:** Integridade criptográfica (hashing) e rastreabilidade de eventos.

## 🛠️ Como utilizar a Ferramenta
1. Abra o arquivo `index.html` em qualquer navegador moderno.
2. Atribua um nível de 0 a 5 para cada critério técnico apresentado.
3. O sistema calculará automaticamente a média por grupo e a classificação estratégica geral.
4. Utilize os botões de exportação para gerar evidências em **CSV**, **JSON** ou **PDF** para processos de auditoria.

## 📊 Arquitetura de Referência
Este controle atua como o **Ponto de Confiança** que valida as identidades (5.16) antes de permitir a autorização (5.15). Sem o 8.5, as permissões concedidas em outros controles perdem sua garantia técnica.
