# Projeto: EduTech-Connect (Sistema Retenção-Grad)


**Objetivo:** Desenvolvimento de uma plataforma inteligente para o Instituto Federal (IFFar) que cruza dados acadêmicos, socioeconômicos e de frequência para emitir alertas e gerenciar planos de intervenção, visando reduzir a evasão nos cursos de graduação.


---


## 1. Roteiro de Entrevista (Stakeholder: Docentes)
Focado em identificar sinais precoces de desinteresse e necessidades do professor em sala de aula.


1. **Sobre engajamento:** Como você percebe, no dia a dia, que um aluno está começando a perder o interesse ou a se desanimar com as suas aulas?
2. **Sobre sinais de risco:** Além das notas baixas e das faltas, que outros comportamentos indicam para você que um aluno tem grandes chances de abandonar o curso?
3. **Sobre atitudes atuais:** O que você costuma fazer hoje quando percebe que um aluno está com dificuldades ou sumindo das aulas?
4. **Sobre envio de alertas:** Qual seria a forma mais rápida e fácil de você avisar no sistema que um aluno não está bem, sem que isso tome muito o seu tempo de aula?
5. **Sobre recebimento de alertas:** Se o sistema pudesse te enviar um aviso automático sobre o histórico de um aluno, que tipo de informação ajudaria você a tentar ajudá-lo a tempo?
6. **Sobre comunicação:** Como o sistema poderia melhorar a sua comunicação com a Coordenação e com o Núcleo de Apoio (psicologia/assistência) para agirem juntos na ajuda a esse aluno?


---


## 2. Questionário Direcionado aos Estudantes
Focado em descobrir quais fatores pesam na decisão de abandonar o curso e os suportes institucionais mais valorizados.


1. De 1 a 5, o quanto sua situação financeira atual dificulta a sua permanência no curso? (1 - Não dificulta nada, 5 - Dificulta muito)
2. O que mais atrapalha suas notas e seu aprendizado nas matérias?
3. Com que frequência você pensa em desistir por achar que talvez tenha escolhido o curso errado?
4. De 1 a 5, que nota você dá para as ajudas do IFFar hoje (bolsas, psicólogo, etc.) comparado ao que você realmente precisa?
5. Que tipo de ajuda do IFFar seria mais importante para garantir que você não desista do curso?


---


## 3. Requisitos Funcionais (Foco na Prevenção da Evasão)
[cite_start]Lista consolidada após o cruzamento de dados das entrevistas (Docentes) e questionários (Estudantes), focando na prevenção e ação proativa[cite: 23, 35].


* **RF01 - Alerta Inteligente de Faltas:** O sistema deve calcular automaticamente padrões de ausência (ex: 3 dias seguidos ou 5 faltas alternadas) e exibir um alerta visual para o professor na tela de chamada.
* **RF02 - Gatilho de Acionamento Rápido:** Durante a chamada, o sistema deve fornecer um botão de "Aviso Rápido" para o professor notificar a Coordenação e a Assistência Estudantil com apenas um clique sobre um aluno em risco.
* **RF03 - Monitoramento de Engajamento no AVA:** O sistema deve monitorar e emitir alertas caso um aluno passe determinado número de dias (ex: 3 dias) sem acessar o Ambiente Virtual de Aprendizagem ou visualizar os materiais postados.
* **RF04 - Mapeamento de Envolvimento Extracurricular:** O sistema deve cruzar dados de participação do aluno em editais, semanas acadêmicas, bolsas de pesquisa e extensão, indicando "baixo envolvimento" se o índice for nulo.
* **RF05 - Painel de Controle de Sobrecarga de Tarefas:** O sistema deve alertar a coordenação e os professores se houver um excesso de trabalhos/tarefas agendados para a mesma turma na mesma semana (mitigando a dor relatada por 50% dos alunos).
* **RF06 - Módulo de Orientação de Carreira:** O sistema deve possuir uma área onde o aluno possa agendar conversas sobre orientação vocacional e de carreira (suporte mais requisitado pelos alunos).
* **RF07 - Portal de Solicitação de Monitoria/Reforço:** O sistema deve permitir que os alunos solicitem rapidamente aulas de reforço ou ajuda de monitores para disciplinas específicas onde encontram dificuldade de compreensão.
* **RF08 - Indicador de Acompanhamento Multidisciplinar:** Na lista de chamada, o sistema deve exibir uma "tag" discreta indicando se o aluno já está recebendo apoio da assistência estudantil ou saúde, sem expor os motivos.
* **RF09 - Histórico de Intervenções Pedagógicas:** O sistema deve manter um registro das metodologias e abordagens didáticas que já foram testadas com o aluno no passado e que surtiram efeito positivo, para consulta rápida dos professores.
* **RF10 - Alerta de Queda Brusca de Produtividade:** O sistema deve identificar e alertar o docente caso um aluno que costumava ter boas entregas passe a entregar trabalhos com atraso frequente ou com qualidade muito inferior.


---


## 4. Requisitos Não Funcionais
Lista de requisitos técnicos fundamentais para o funcionamento do Retenção-Grad.


* **RNF01 - Privacidade e Segurança (LGPD):** O sistema deve garantir o anonimato de dados sensíveis e operar com perfis de acesso restritos[cite: 28]. Professores terão acesso apenas ao histórico pedagógico e a "tags" de acompanhamento genéricas, enquanto dados psicológicos e socioeconômicos detalhados serão visíveis exclusivamente pelo Núcleo de Apoio ao Estudante (CAE/SAP/SRA).
* **RNF02 - Disponibilidade e Confiabilidade:** O sistema deve garantir uma alta disponibilidade (uptime de 99,9%), possuindo infraestrutura escalável (como servidores em nuvem) para evitar quedas e lentidão durante os períodos críticos, como semanas de provas, fechamento de notas e rematrículas.
* **RNF03 - Performance e Predição:** O sistema deve ser capaz de processar os cruzamentos de dados (frequência, notas, engajamento no AVA) em segundo plano, garantindo que a emissão de alertas na interface do professor (durante a chamada) ocorra em tempo real, sem travamentos.
