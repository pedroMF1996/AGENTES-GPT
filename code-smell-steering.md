---
inclusion: auto
name: "code-smells"
description: "Use automaticamente sempre que houver qualquer análise, modificação ou geração de código para identificar, prevenir e corrigir problemas de qualidade (code smells), incluindo cenários como implementação, correção de bugs, refatoração, revisão de código ou melhoria de legibilidade, estrutura ou manutenibilidade."
---

# Code Smells

Lista estruturada dos principais code smells com seus respectivos nomes e descrições detalhadas. Use esta skill sempre que o usuário precisar consultar, entender ou aplicar correções relacionadas a code smells, ou quando houver necessidade de avaliar a qualidade do código com base em problemas conhecidos de design e implementação. 

Regra obrigatória:  
Todo Code Smell identificado deve ser corrigido automaticamente através de refatoração apropriada. Siga os principios de refatoração descritos em `refactoring-mf`

- Função grande  
  → Difícil de entender sem dividir em partes menores.  
- Classe grande  
  → Indica múltiplas responsabilidades.  
- Muitos parâmetros  
  → Indica necessidade de melhor modelagem.  
- Duplicação  
  → Mesma lógica repetida em múltiplos lugares.  
- Comentários excessivos  
  → Código não é autoexplicativo.  
- Código morto  
  → Código que não é executado.  
- Dependência cíclica  
  → Módulos dependem mutuamente.  
- Excesso de condicionais  
  → Indica falta de abstração adequada.  
