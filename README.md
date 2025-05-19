# Projeto de Simulação de Fluxo de Notícias com Agentes de IA



## Contexto



Este projeto foi desenvolvido como parte da **Imersão Alura + Google Gemini 2025**, focado na exploração e aplicação prática dos modelos de Inteligência Artificial do Google Gemini.



## Objetivo



O principal objetivo deste projeto é iniciar o entendimento sobre o funcionamento e a orquestração de **modelos e agentes de Inteligência Artificial**. Através da simulação de um pipeline automatizado de agregação, planejamento, redação e revisão de notícias, exploramos como diferentes agentes de IA, cada um com uma função específica, podem colaborar para atingir um resultado complexo.



## Visão Geral do Projeto



O projeto simula um fluxo de trabalho de uma agência de notícias utilizando quatro agentes de IA especializados. Cada agente recebe a saída do agente anterior e executa sua tarefa com base em prompts definidos, culminando em um post de notícia revisado pronto para leitura.



## Arquitetura e Fluxo dos Agentes



O sistema é composto por quatro agentes de IA que trabalham em sequência:



1.  **Agente BUSCADOR**

    * **Função:** Iniciar o processo buscando informações recentes.

    * **Detalhes:** Realiza buscas no Google para encontrar notícias e acontecimentos relevantes do último mês.

    * **Entrada:** Um prompt inicial definindo o escopo da busca (Ex: "últimas notícias de tecnologia no Brasil").

    * **Saída:** Uma lista inicial de manchetes ou links de notícias encontradas.

    * **Próximo:** Passa a lista de notícias para o Agente PLANEJADOR.



2.  **Agente PLANEJADOR**

    * **Função:** Aprofundar a pesquisa sobre os tópicos identificados.

    * **Detalhes:** Recebe as notícias do Agente BUSCADOR e realiza novas buscas no Google para obter mais detalhes e contexto sobre cada item, seguindo critérios definidos por um prompt.

    * **Entrada:** A lista de notícias do Agente BUSCADOR e um prompt com instruções para detalhamento da pesquisa.

    * **Saída:** Um planejamento ou resumo detalhado das notícias, contendo informações essenciais para a redação.

    * **Próximo:** Passa o planejamento para o Agente REDATOR.


3.  **Agente REDATOR**

    * **Função:** Compor o post da notícia.

    * **Detalhes:** Recebe o planejamento detalhado e redige um post de notícia completo, seguindo o estilo, formato e requisitos definidos por um prompt específico de redação.

    * **Entrada:** O planejamento detalhado do Agente PLANEJADOR e um prompt com as instruções de redação.

    * **Saída:** O rascunho inicial do post da notícia.

    * **Próximo:** Passa o rascunho para o Agente REVISOR.


4.  **Agente REVISOR**

    * **Função:** Garantir a qualidade e adequação do texto final.

    * **Detalhes:** Recebe o rascunho do Agente REDATOR e realiza uma revisão completa, verificando gramática, ortografia, coesão, clareza e aderência às instruções de redação.

    * **Entrada:** O rascunho do post do Agente REDATOR e o prompt original de redação (ou um prompt de revisão).

    * **Saída:** O post da notícia revisado e finalizado.

    * **Próximo:** Apresenta o post finalizado ao "leitor" (neste caso, a saída final do programa).


## Tecnologias Utilizadas


* **Modelos de IA:** Google Gemini (gemini-2.0-flash)

* **SDK/API:** Google AI Python SDK

* **Busca Web:** [Google Search API]

* **Linguagem:** Python

## Ana Julia Reis de Mattos

##README estruturado com o auxílio de Inteligência Artificial
