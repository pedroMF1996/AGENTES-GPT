---
inclusion: auto
name: "clean-code"
description: "Use automaticamente sempre que houver escrita, modificação ou revisão de código para garantir legibilidade, clareza, boas práticas e qualidade estrutural, incluindo cenários como implementação de funcionalidades, correção de bugs, refatoração, criação de testes ou qualquer alteração que envolva código."
---

# Clean Code Principles

##### 1. Nomes (Naming)
- Programe sempre em pt-BR
- Use nomes que revelam intenção  
  → O nome deve permitir entender o comportamento sem abrir a implementação.  
- Evite abreviações desnecessárias  
  → Só use abreviações amplamente conhecidas no domínio.  
- Evite desinformação  
  → O nome deve refletir corretamente o tipo, estrutura ou comportamento real.  
- Use nomes pronunciáveis  
  → Devem ser fáceis de falar em comunicação verbal.  
- Use nomes pesquisáveis  
  → Evite nomes curtos/genéricos que dificultam busca no código.  
- Evite prefixos/sufixos redundantes  
  → Não repita informação já evidente pelo contexto.  
- Evite codificação de tipo  
  → O tipo já é definido pela linguagem, não pelo nome.  
- Classes → substantivos  
  → Representam entidades ou conceitos.  
- Métodos → verbos  
  → Representam ações executadas.  
- Evite trocadilhos semânticos  
  → Não use o mesmo nome com significados diferentes.  
- Use consistência de vocabulário  
  → Um conceito deve ter sempre o mesmo nome no sistema.  
- Evite nomes genéricos  
  → Evite nomes que não indicam responsabilidade.  
- Prefira clareza a concisão  
  → O nome deve reduzir esforço de leitura.  

##### 2. Funções
- Devem ser pequenas  
  → Devem caber em uma tela sem necessidade de rolagem.  
- Fazer apenas uma coisa  
  → Deve executar uma única responsabilidade sem múltiplos objetivos.  
- Nível de abstração único  
  → Todas as instruções devem operar no mesmo nível de detalhe.  
- Evitar switch quando cresce  
  → Muitos casos indicam necessidade de abstração por polimorfismo.  
- Nome descritivo baseado em efeito  
  → Deve indicar claramente o resultado produzido.  
- Poucos parâmetros  
  → Ideal até 3; acima disso aumenta complexidade de uso e portanto criamos um DTO.  
- Evitar flags booleanas  
  → Um booleano indica múltiplos comportamentos na mesma função.  
- Preferir objeto de parâmetros  
  → Agrupa dados relacionados em uma única estrutura.  
- Sem efeitos colaterais ocultos  
  → Não deve alterar estado externo sem deixar explícito.  
- Não usar parâmetros de saída  
  → Não modificar argumentos para retornar valores.  
- Separar comando de consulta  
  → Ou altera estado ou retorna valor, nunca ambos.  

##### 3. Comentários
- Comentários são último recurso  
  → Só usar quando o código não consegue expressar a intenção.  
- Explique o porquê  
  → Justifique decisões, não descreva o que o código faz.  
- Documentar APIs públicas  
  → Explicar uso, contrato e restrições.  
- Evitar redundância  
  → Não repetir o que já está evidente no código.  
- Evitar comentários enganosos  
  → Devem estar sempre corretos.  
- Evitar comentários desatualizados  
  → Devem evoluir junto com o código.  
- Evitar comentários óbvios  
  → Não adicionar informação irrelevante.  

##### 4. Formatação
- Código deve ser escaneável  
  → Estrutura deve ser compreendida rapidamente ao bater o olho.  
- Espaçamento separa conceitos diferentes  
  → Use linha em branco quando muda o contexto lógico.  
- Agrupar código relacionado  
  → Linhas que participam da mesma lógica devem ficar juntas, sem código não relacionado entre elas.  
- Indentação consistente  
  → Deve refletir a hierarquia de execução.  
- Linhas curtas  
  → Evitam quebra de leitura horizontal.  
- Ordem interna previsível  
  → Organização consistente dentro de classes.  
- Leitura top-down  
  → Métodos de alto nível aparecem antes dos detalhes.  

##### 5. Objetos e Estruturas (Usar entidades ricas apenas se o projeto ja usar entidades anemicas continuar usando entidades anemicas)
- Objetos encapsulam comportamento  
  → Regras de negócio devem estar dentro do objeto.  
- Estruturas expõem dados  
  → Usadas apenas para transporte de dados.  
- Não misturar os dois  
  → Evitar objetos que expõem dados e também possuem lógica.  
- Preferir objetos quando há comportamento  
  → Centraliza regras e reduz duplicação.  
- Evitar getters/setters triviais  
  → Indicam ausência de encapsulamento real.  
- DTOs sem lógica  
  → Devem apenas transportar dados.  

##### 6. Tratamento de Erros
- Usar exceções para erro  
  → Separar erro do fluxo normal.  
- Separar fluxo normal do erro  
  → Caminho principal deve ser legível sem interrupções.  
- Mensagens claras e diagnósticas  
  → Devem permitir identificar causa do problema.  
- Evitar null  
  → Evita estados ambíguos.  
- Não ignorar exceções  
  → Sempre tratar ou propagar corretamente.  
- Não mascarar erro original  
  → Preservar contexto do erro.  
- Minimizar lógica em catch  
  → Apenas tratar, logar ou adaptar.  

##### 7. Testes
- Código deve ser testável  
  → Dependências controladas e isoladas.  
- Testes rápidos 
  → Devem executar em pouco tempo.  
- Independentes  
  → Não dependem de estado externo ou ordem de execução.  
- Determinísticos  
  → Mesmo input gera sempre o mesmo resultado.  
- Auto-validáveis  
  → Não exigem análise manual.  
- Criados junto com o código  
  → Evita lacunas de cobertura.  
- Uma responsabilidade por teste  
  → Facilita identificar falhas.  
- Nome descritivo  
  → Explica cenário e resultado esperado.  
- Estrutura AAA  
  → Separar preparação, execução e verificação.  

##### 8. Classes
- Classes pequenas  
  → Fáceis de entender rapidamente.  
- Responsabilidade única  
  → Uma única razão para mudança.  
- Alta coesão  
  → Métodos operam sobre o mesmo conjunto de dados e objetivo.  
- Baixo acoplamento  
  → Pouca dependência de outras classes.  
- Evitar classe “Deus”  
  → Não concentrar múltiplas responsabilidades.  
- Poucos campos de estado  
  → Indica foco claro.  
- Preferir composição  
  → Delegar comportamento ao invés de herdar.  

##### 9. Arquitetura (Analisar e seguir o padrão ja implementado nos projetos, mas se, e apenas se, o projeto estiver faltando com uma arquitetura definida) 
- Separar responsabilidades por camada  
  → UI lida com entrada/saída, domínio com regras, infraestrutura com tecnologia.  
- Inversão de dependência  
  → Camadas de alto nível não dependem de detalhes técnicos.  
- Baixo acoplamento entre módulos  
  → Mudanças não devem se propagar facilmente.  
- Domínio isolado  
  → Regras de negócio independentes de frameworks.  
- Interfaces como contratos  
  → Definem comportamento sem acoplar implementação.  
- Evitar estado global  
  → Evita dependências ocultas.  
- Inicialização separada  
  → Configuração fora da lógica de negócio. 

##### 10. SOLID
- SRP  
  → Uma unidade tem uma única razão para mudar.  
- OCP (Como nossos objetos de trabalho estão sempre em mudança esse principio é muito dificil de ser seguido)
  → Código pode ser estendido sem modificação. 
- LSP  
  → Subtipos podem substituir tipos base sem quebrar comportamento.  
- ISP  
  → Interfaces devem ser específicas ao cliente.  
- DIP  
  → Depender de abstrações, não de implementações.  

##### 11. Código Limpo Geral
- Legibilidade como prioridade  
  → Código deve ser fácil de entender.  
- Evitar duplicação (DRY)  
  → Uma regra deve existir em um único lugar.  
- Evitar complexidade (KISS)  
  → Preferir soluções simples.  
- Não implementar antes da necessidade (YAGNI)  
  → Evitar código não utilizado.  
- Refatorar continuamente  
  → Melhorar estrutura sem alterar comportamento.  
- Remover código morto  
  → Eliminar código não utilizado.  
- Manter código sempre funcional  
  → Não deixar código quebrado no repositório.  

##### 12. Concorrência
- Evitar estado compartilhado  
  → Reduz risco de condições de corrida.  
- Preferir imutabilidade  
  → Estado não muda após criação.  
- Sincronização mínima  
  → Usar apenas quando necessário.  
- Threads independentes  
  → Execuções não devem depender entre si.  
- Seções críticas pequenas  
  → Reduz contenção e melhora desempenho.  

##### 13. Variáveis
- Declarar próximo do uso  
  → A variável deve ser declarada imediatamente antes (ou o mais próximo possível) da primeira linha onde é utilizada.  
- Escopo mínimo  
  → A variável deve existir apenas dentro do menor bloco onde é necessária.  
- Inicializar na declaração  
  → Atribuir valor no momento da criação.  
- Evitar variáveis intermediárias desnecessárias  
  → Não criar variáveis que não agregam clareza.  
- Não reutilizar variáveis para propósitos diferentes  
  → Uma variável deve representar um único significado.  
- Preferir imutáveis  
  → Evitar reatribuição após inicialização.  
- Evitar variáveis globais  
  → Reduz dependência implícita.  
- Tipos expressivos  
  → Tipo deve comunicar claramente o propósito.
