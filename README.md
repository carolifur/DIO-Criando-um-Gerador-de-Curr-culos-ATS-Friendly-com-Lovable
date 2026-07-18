# DIO-Criando-um-Gerador-de-Curr-culos-ATS-Friendly-com-Lovable
Gerador de currículos otimizados para sistemas ATS (Applicant Tracking Systems), desenvolvido com a plataforma Low-Code Lovable. O projeto visa criar currículos altamente legíveis por inteligências artificiais de recrutamento, formatando seções de forma estratégica e automática para aumentar as chances de aprovação em processos seletivos.

Projeto: Otimiza Vagas — ATS-Friendly Resume Optimizer (MVP)

Você é um desenvolvedor frontend especialista em React, Tailwind CSS e UI/UX. Seu objetivo é construir o MVP do Otimiza Vagas, um otimizador de currículos amigável para sistemas ATS (Applicant Tracking Systems) que também ajuda o usuário a encontrar vagas abertas reais na internet baseadas no seu perfil profissional.

A aplicação deve ser totalmente funcional, altamente intuitiva e seguir rigorosamente as diretrizes do Google Material Design (Material 3), focando em acessibilidade (Design Universal), cantos suavemente arredondados, elevações sutis e tipografia perfeitamente legível.

🔴 REGRAS CRÍTICAS E PREMISSAS

Login Social Simples: A aplicação deve exigir ou permitir o login rápido através da Conta Google (Google Sign-In).

Memorização e Persistência de Dados (Sem Re-upload): Uma vez que o usuário faça login no Otimiza Vagas e suba seu currículo pela primeira vez, a aplicação deve salvar automaticamente esses dados na conta do usuário (usando Supabase ou persistência local atrelada ao ID do Google). Nas próximas visitas, o usuário entra direto no seu painel com o currículo salvo, sem necessidade de re-upload.

Sem Alucinações (Ética de Dados): O sistema nunca deve inventar experiências, formações, anos de atuação, projetos ou qualificações. Ele deve apenas reorganizar, polir e otimizar a linguagem dos dados existentes no currículo para que passem melhor em filtros ATS.

Acessibilidade e Alto Contraste: A interface deve seguir estritamente as diretrizes da WCAG, garantindo um excelente contraste de cores entre os textos e os fundos (mínimo de 4.5:1 para texto normal) para evitar fadiga visual e facilitar a leitura de qualquer usuário.

SEO & Webwriting (Escaneabilidade): O layout e os textos da aplicação devem aplicar técnicas de Webwriting. Use microtextos claros, títulos diretos (H1, H2, H3), parágrafos curtos, negritos em palavras-chave e listas com marcadores (bullet points). A estrutura HTML do app deve ser semanticamente correta para seguir as melhores práticas de SEO técnico.

Sem APIs de Vagas Complexas (Simplicidade de Infraestrutura): Para exibir vagas abertas reais na internet sem precisar assinar APIs pagas, gere links dinâmicos e inteligentes de busca (Deep Links) para grandes agregadores (LinkedIn Jobs, Google Jobs, Indeed, Infojobs) com base nas palavras-chave do usuário, ou utilize um leitor de feed RSS público/busca estruturada simulada no cliente que retorne listagens reais em cards.

🎨 PALETA DE CORES (Base: Azure Acinzentado Pastel)

Utilize rigorosamente a seguinte paleta, garantindo taxas de contraste ideais (Texto Escuro sobre Fundos Claros):

Primary (Azure Pastel): #A3B8CC (Um azul acinzentado suave e profissional)

Secondary (Cinza Médio Frio): #6C7D8C

Background / Surface: #F4F6F8 (Off-white acinzentado muito limpo e confortável para leitura)

On-Surface / Text: #2C3539 (Grafite escuro para excelente contraste)

Accent / Highlight: #D1E0EC (Para estados de foco, seleção ou hovers sutis)

Error: #BA1A1A / Success: #2E7D32

🚀 FLUXO DO USUÁRIO E SEÇÕES DA INTERFACE

📍 Indicador de Progresso (Stepper Superior)

Exiba fixo no topo da aplicação uma barra de progresso linear e acessível (Stepper) indicando visualmente as etapas do processo: 1. Início ➔ 2. Perfil ➔ 3. Escolha da Vaga ➔ 4. Otimização ➔ 5. Download.

1. Tela de Entrada & Autenticação (Passo 1)

Exiba uma landing page limpa do Otimiza Vagas, aplicando técnicas de Webwriting com propostas de valor claras.

Botão oficial de "Entrar com o Google".

Verificação de Retorno: Se o usuário já possuir um currículo salvo na conta, pule o upload e vá direto para o Painel Principal (Dashboard).

2. Upload do Currículo & LinkedIn (Passo 2 - Novos Usuários)

Upload de Arquivo: Dropzone minimalista para arquivos em PDF, DOCX ou TXT.

Perfil do LinkedIn: Input de texto para colar o link do perfil.

Salvamento Automático: Salve estes dados imediatamente na sessão do usuário.

3. Painel Principal (Dashboard de Vagas e Currículo Salvo - Passo 3)

Exiba um resumo do currículo que está guardado na conta (com opção de atualizar o arquivo se desejado).

Buscador de Vagas Recomendadas: Seção com cards de vagas reais baseadas nas competências do currículo salvo. Cada card deve ter: Título, Empresa, Localização e Link Direto.

Botão de destaque no card: "Otimizar meu Currículo para esta Vaga" para iniciar a análise comparativa imediata no Otimiza Vagas.

4. Tela de Análise Comparativa & Carregamento (Passo 4)

Estado de Esqueleto (Skeleton Screens): Enquanto a análise está sendo processada, exiba blocos cinzas pulsantes simulando o layout estrutural do relatório para melhorar a percepção de velocidade.

Match Score: Um indicador visual e acessível de compatibilidade (gráfico circular ou barra de progresso).

Palavras-chave Faltantes: Lista clara de termos técnicos que a vaga pede mas o currículo não destaca.

Sugestões de Ajustes: Cards objetivos apontando melhorias de escrita e estrutura.

5. Editor de Currículo Otimizado (Passo 5)

Visualização Antes vs. Depois: Exiba um painel dividido (ou um botão de alternância rápido) para o usuário comparar o texto original com a versão sugerida pela otimização.

Edição Manual Direct-on-Page: O usuário clica e edita qualquer bloco de texto (Resumo, Experiência, Formação) diretamente na tela.

Botão Restaurar Original: Ao lado ou dentro de cada bloco editável, forneça uma ação discreta de "Desfazer" ou "Restaurar sugestão inicial" para dar total controle e segurança ao usuário.

Design Clean (ATS Friendly): Layout de coluna única, sem gráficos de barra de habilidades ou tabelas complexas, usando fontes limpas e espaçamento legível.

6. Finalização e Exportação (Botão Indicativo)

Botão de ação flutuante ou fixo destacado: "Meu Currículo está Pronto!" (com ícone de check).

Ao clicar, abre um modal de conclusão apresentando as opções:

Baixar PDF: Geração de arquivo PDF com texto 100% selecionável (essencial para leitura de sistemas ATS).

Compartilhar: Permite copiar o texto limpo para a área de transferência ou gerar um link de compartilhamento rápido.

https://github.com/carolifur/DIO-Criando-um-Gerador-de-Curr-culos-ATS-Friendly-com-Lovable/blob/main/OTIMIZA1.jpg

https://github.com/carolifur/DIO-Criando-um-Gerador-de-Curr-culos-ATS-Friendly-com-Lovable/blob/main/OTIMIZA2.jpg

https://github.com/carolifur/DIO-Criando-um-Gerador-de-Curr-culos-ATS-Friendly-com-Lovable/blob/main/OTIMIZA3.jpg

https://github.com/carolifur/DIO-Criando-um-Gerador-de-Curr-culos-ATS-Friendly-com-Lovable/blob/main/OTIMIZA4.jpg

https://github.com/carolifur/DIO-Criando-um-Gerador-de-Curr-culos-ATS-Friendly-com-Lovable/blob/main/OTIMIZA5.jpg
