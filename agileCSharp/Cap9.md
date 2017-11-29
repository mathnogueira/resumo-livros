# Open-Closed Principle

- "Todos os sistemas mudam durante seus ciclos de vida"

## Sintomas
    - Software rígido
    - Mudanças de comportamento requerem mudanças em vários arquivos;

## Resumo

- Módulos são abertos para ampliação
    - Novos comportamentos podem ser inseridos no módulo
        - Strategy + Abstraction
- Módulos são fechados para modificação
    - Para suportar novos comportamentos, o módulo não deve ser alterado

- if-else e switches não são sustentáveis
- O uso de polimorfismo causa dois pontos positivos:
    - Mudanças são isoladas em classes distintas e não impactam as demais classes;
    - Adição de novos comportamentos são mais simples e não demandam a modificação de outras classes.

## Desafios
    - Antecipação das possíveis mudanças que podem ocorrer;
    - Construção de um modelo que possa atender a todas as possíveis mudanças;
    - Não existe um modelo que seja natural para todos os contextos.