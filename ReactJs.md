React/JSX Style patterns
=============

1. [Regras Básicas](#basic-rules)
2. [Hierarquia de Componentes](#components)
3. [Importações](#imports)

## 1. Regras Básicas

- .jsx: Para arquivos que exportam apenas um componente React.

- .js: Para arquivos que exportam uma ou várias funções e constantes que não retornam componentes React.

## 2. Nomenclatura
### 2.1 Nomenclatura de Componentes
- Componentes Principais: 
 - Serão exportados diretamente para uma rota, tendo o mesmo nome desta. Seguem o padrão: *NomeDoArquivo.jsx*

- Componentes Secundários: 
 - Componentes que servem para a construção dos componentes principais, tendo o nome de partes de um site, como *navbar* e *card*. Seguem o padrão: *ArquivoPrincipal.nome-do-secundário.jsx*.

- Componentes Construtores:
 - São entendidos como componentes de construção para componentes secundários e outros contrutores. Basicamente, é bem difícil que eles sejam escritos em componentes principais. Seguem o padrão: "nome_do_arquivo.jsx"
 
- Componentes Reutilizáveis: 
 - Componentes que estão presentes dentro da pasta `reusableCoponents`, usam o padrão "CL.nome-do-arquivo", onde CL são as duas letras da abreviação da empresa.

### 2.2 Nomenclatura de Pastas
Todas as pastas seguem o padrão 'nomeDaPasta'. Dentro da pasta `src` temos X pastas mães:

- `assets`: Pasta que contém as imagens e pode conter arquivos de css.

- `services`: Pasta que tem os arquivos que preparam a api e fazem a autenticação do usuário.

- `context`: Pasta que tem os arquivos que criarão o contexto usando o *useContext*.

- `languages`: Pasta que contém todos os arquivos relacionados a tradução.

- `reusableComponents`: Pasta para componentes que podem ser reutilizados de maneira genérica por outras partes do código.

- `pages`: Pasta que contém outras pastas com nomes de rota, cada uma dessas pastas pode ter várias outras pastas dentro, mas apenas um arquivo imediato.

### 2.3 Exemplos de Arquitetura
A maioria das pastas seguem a seguinte hierarquia:
- nomeDaRota
 - ArquivoPrincipal.jsx
 - constructors
   - ArquivoPrincipal.parte-1.jsx
   - ArquivoPrincipal.parte-2.jsx
   - parte1
     - nome_da_construção.jsx
   - parte2
     - nome_da_construção.jsx

Pasta `reusableComponents`:
- `reusableComponents`
 - feature
   - CL.feature-name.jsx
 - constructors
   - ArquivoPrincipal.parte-1.jsx
   - ArquivoPrincipal.parte-2.jsx
   - parte1
     - nome_da_construção.jsx
   - parte2
     - nome_da_construção.jsx



## 3. Importações
Dentro da ordenação, existe a seguinte hierarquia: Funções > Componentes > Imagens > Ícones e Estilos.

1° Importações do `React`

2° Importações de `api` e `context` 

3° Importações de `Node Modules`

4° Importações de `reusableComponents`

5° Importações .jsx de outros lugares

6° Importações de Imagens

7° Importações de Estilos

OBS.: Uma vez que se saia de um nível da hierarquia para o outro é preciso pular uma linha.
