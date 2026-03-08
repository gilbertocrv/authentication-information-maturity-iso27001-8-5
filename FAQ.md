# FAQ – Secure Authentication (ISO 8.5)

### 1. Por que o Controle 8.5 é separado do 5.17 (Authentication Information)?
Enquanto o **5.17** foca na gestão da informação de autenticação (como as senhas são criadas, trocadas e protegidas), o **8.5** foca no **mecanismo técnico** de validação. O 5.17 é a "regra de negócio" da credencial; o 8.5 é a "tecnologia" que garante que o processo de login seja seguro.

### 2. O que define uma autenticação como "MFA Real" segundo a norma?
Para ser considerado MFA, é necessário utilizar pelo menos dois fatores de categorias diferentes:
* **Algo que você sabe:** Senha ou PIN.
* **Algo que você tem:** Token físico, App autenticador ou Smartcard.
* **Algo que você é:** Biometria.
Dois fatores da mesma categoria (ex: senha + pergunta de segurança) não cumprem o rigor técnico de um MFA moderno.

### 3. Como o Step-Up Authentication ajuda na redução de riscos?
O Step-Up reduz a fricção para o usuário em tarefas comuns, mas exige prova extra de identidade para tarefas de alto risco (ex: mudar uma senha de administrador ou realizar uma transferência). Isso impede que um atacante que sequestrou uma sessão básica cause danos críticos.

### 4. Quais são os métodos de Hashing recomendados para o armazenamento de credenciais?
Devem ser utilizados algoritmos de hash resistentes a ataques de colisão e força bruta (GPU cracking), como **Argon2** ou **bcrypt**, sempre utilizando *salt* individual para cada credencial.

### 5. Como medir o sucesso deste controle?
Através de indicadores (KPIs) como:
* % de usuários críticos com MFA ativo.
* Número de tentativas de login suspeitas bloqueadas pelo RBA.
* Tempo médio para detecção de anomalias em logs de autenticação.