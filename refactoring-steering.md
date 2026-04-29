---
inclusion: auto
name: "refactoring-mf"
description: "Use sempre que houver necessidade de melhorar a estrutura do código sem alterar comportamento, incluindo cenários como correção de code smells, simplificação de lógica, redução de complexidade, remoção de duplicação ou quando o código estiver difícil de entender, manter ou evoluir."
---

# Refactoring Principles

Princípios a serem seguidos na refatoração de código no desenvolvimento de software, com foco em melhorar a estrutura interna sem alterar o comportamento externo. Siga essas regras para implementar boas refatorações:

##### 1. Composing Methods
- Extract Method  
  → Mover um trecho de código para um novo método quando ele pode ser nomeado de forma significativa.  
- Inline Method  
  → Substituir a chamada de um método pelo seu conteúdo quando ele não agrega abstração.  
- Extract Variable  
  → Criar variável para armazenar uma expressão complexa, tornando-a legível.  
- Inline Variable  
  → Remover variável intermediária quando ela não melhora a clareza.  
- Change Function Declaration  
  → Alterar nome ou parâmetros para refletir melhor o comportamento real.  
- Replace Temp with Query  
  → Substituir variável temporária por uma função que calcula o valor.  
- Split Variable  
  → Dividir uma variável que assume múltiplos significados.  
- Remove Assignments to Parameters  
  → Evitar alterar parâmetros; usar variável local ao invés disso.  
- Replace Method with Method Object  
  → Transformar método complexo em uma classe para facilitar manipulação de estado.  

##### 2. Moving Features Between Objects
- Move Function  
  → Mover método para a classe onde os dados que ele usa estão concentrados.  
- Move Field  
  → Mover atributo para a classe que mais o utiliza.  
- Move Statements into Function  
  → Mover código repetido para dentro de uma função específica.  
- Move Statements to Callers  
  → Mover comportamento para quem chama quando ele não é geral.  
- Split Phase  
  → Separar uma operação em fases distintas.  

##### 3. Organizing Data
- Encapsulate Record  
  → Transformar estrutura de dados em objeto com métodos controlando acesso.  
- Encapsulate Collection  
  → Evitar exposição direta de coleções. 
- Replace Primitive with Object  
  → Substituir tipos primitivos por objetos de domínio.  
- Replace Temporary Variable with Query  
  → Substituir variável temporária por cálculo direto via método.  
- Extract Class  
  → Separar responsabilidades de uma classe em duas.  
- Inline Class  
  → Unir classes quando separação não agrega valor.  
- Remove Middle Man  
  → Eliminar classe intermediária que apenas delega chamadas.  
- Introduce Parameter Object  
  → Agrupar parâmetros relacionados em um objeto.  

##### 4. Simplifying Conditional Logic
- Decompose Conditional  
  → Separar condição, ação e alternativa em métodos distintos.  
- Consolidate Conditional Expression  
  → Unificar múltiplas condições equivalentes.  
- Replace Nested Conditional with Guard Clauses  
  → Substituir estruturas aninhadas por retornos antecipados.  
- Replace Conditional with Polymorphism  
  → Usar classes ao invés de condicionais.  
- Introduce Assertion  
  → Validar condições que devem sempre ser verdadeiras.  

##### 5. Simplifying Method Calls
- Rename Method  
  → Nomear método de forma mais representativa.  
- Add Parameter  
  → Adicionar parâmetro necessário.  
- Remove Parameter  
  → Remover parâmetros não utilizados.  
- Separate Query from Modifier  
  → Separar leitura de alteração de estado.  
- Parameterize Method  
  → Generalizar comportamento com parâmetros.  
- Replace Parameter with Explicit Methods  
  → Criar métodos distintos ao invés de flags.  
- Preserve Whole Object  
  → Passar objeto completo ao invés de dados isolados.  

##### 6. Dealing with Generalization
- Pull Up Method  
  → Mover método comum para superclasse.  
- Pull Up Field  
  → Mover atributo comum para superclasse.  
- Push Down Method  
  → Mover método específico para subclasses.  
- Push Down Field  
  → Mover atributo para subclasses específicas.  
- Extract Superclass  
  → Criar superclasse para comportamento comum.  
- Collapse Hierarchy  
  → Remover hierarquia desnecessária.  
- Replace Inheritance with Delegation  
  → Usar composição ao invés de herança.  
- Replace Delegation with Inheritance  
  → Usar herança quando adequado.  

##### 7. Encapsulation
- Encapsulate Field  
  → Tornar campo privado e controlar acesso.  
- Replace Data Value with Object  
  → Substituir valor simples por objeto com comportamento.  
- Replace Type Code with Class  
  → Substituir código por classe.  
- Replace Type Code with Subclasses  
  → Usar subclasses ao invés de códigos.  
- Replace Type Code with State/Strategy  
  → Usar padrões ao invés de condicionais.  

##### 8. General Cleanup
- Remove Dead Code  
  → Remover código não utilizado.  
- Substitute Algorithm  
  → Trocar implementação por uma mais clara, sem alterar a funcionalidade existente.
- Introduce Explaining Variable  
  → Criar variável para explicar expressão.  
- Split Loop  
  → Separar loops com múltiplas responsabilidades.  
- Replace Loop with Pipeline  
  → Usar abordagem declarativa (ex: LINQ, map, etc). 
