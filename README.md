
# Opções ISS 2 (Multi2) v0.1 | Fabio FJA

**Editor de configurações do ISS Pro Evolution 2 para PlayStation 1**

**Desenvolvido por Fabio FJA | Delphi | Object Pascal | Windows**

## Sobre o projeto

O Opções ISS 2 (Multi2) v0.1 é uma ferramenta de edição e personalização do ISS Pro Evolution 2 para PlayStation 1 (PSX), desenvolvida em Delphi utilizando a linguagem Object Pascal.

O programa permite modificar configurações internas do jogo que normalmente exigiriam a utilização de um editor hexadecimal.

Por meio de uma interface gráfica, é possível remover equipes dos menus de seleção, restaurar bandeiras, modificar a velocidade das partidas, ajustar configurações da Master Liga e da Liga, alterar limites de contratações e desbloquear opções de competições.

A ferramenta utiliza técnicas de engenharia reversa e modificação de arquivos binários por meio de offsets previamente identificados.

## Funcionalidades

### 1. Editor gráfico de equipes (Team Remover)

Uma das principais funcionalidades do programa é o editor de equipes, inspirado na ferramenta Team Remover by Cuervo.

- Exibição gráfica das bandeiras das equipes.
- Seleção das equipes diretamente pelas imagens.
- Remoção individual de equipes da lista de seleção.
- Alteração dos dados de equipes no arquivo BIN.
- Interface visual com 54 posições de bandeiras editáveis.
- Avisos de segurança ao remover as posições iniciais dos jogadores 1 e 2.

O editor modifica os identificadores internos correspondentes às equipes, permitindo personalizar os menus de seleção do jogo.

### 2. Restauração das bandeiras

- Restauração dos dados de equipes anteriormente modificados.
- Recuperação da organização das bandeiras por meio do arquivo auxiliar `bandeiras.bin`.
- Atualização visual dos elementos do editor.

**Importante:** o arquivo `bandeiras.bin` deve permanecer na mesma pasta do programa para que a restauração funcione.

### 3. Desbloqueio de equipes

- Opção para habilitar todas as equipes.
- Modificação de offsets responsáveis pelas restrições de seleção.
- Possibilidade de restaurar os valores anteriores dos parâmetros de desbloqueio.
- Ampliação das opções de equipes disponíveis no jogo.

### 4. Controle de velocidade das partidas

Permite alterar a velocidade do jogo utilizando três configurações:

- **Normal:** velocidade original.
- **Máxima:** velocidade aumentada.
- **Turbo:** configuração de velocidade ainda mais elevada.

As alterações são realizadas diretamente nos parâmetros internos do arquivo BIN.

### 5. Personalização da Master Liga

**Dinheiro inicial**
- 0 créditos.
- 20 créditos.
- 999 créditos.

**Limite de contratações**
- Configuração original de 2.
- Configuração ampliada com valor 255.

**Tempo das partidas**
- 5, 10, 15, 20, 25 ou 30 minutos.

**Dificuldade**
- Fácil.
- Normal.
- Difícil.

### 6. Personalização do modo Liga

Permite modificar as configurações das partidas da Liga.

**Tempo disponível**
- 5, 10, 15, 20, 25 ou 30 minutos.

**Níveis de dificuldade**
- Fácil.
- Normal.
- Difícil.

### 7. Desbloqueio do menu de Copas

- Modificação de parâmetros internos relacionados ao menu de Copas.
- Opção específica para destravar o menu.
- Aplicação direta da alteração no arquivo do jogo.

### 8. Manipulação de arquivos BIN

- Seleção do arquivo BIN pela interface gráfica do Windows.
- Gravação direta de bytes em offsets específicos.
- Alteração de configurações sem necessidade de um editor hexadecimal externo.
- Mensagens de confirmação em diferentes operações.

## Tecnologias utilizadas

- **Linguagem:** Object Pascal
- **Ambiente de desenvolvimento:** Borland Delphi
- **Interface gráfica:** Visual Component Library (VCL)
- **Plataforma:** Microsoft Windows
- **Manipulação binária:** arquivos tipados e TFileStream
- **Recursos gráficos:** componentes TImage e imagens BMP/JPG
- **Jogo:** ISS Pro Evolution 2 (PS1)
- **Formato de distribuição:** executável Windows (.exe)

## Estrutura do projeto

**Unit1.pas:** código-fonte principal, incluindo operações de edição e gravação binária.

**Unit1.dfm:** interface gráfica desenvolvida no Delphi.

**Project1.dpr:** arquivo principal do projeto Delphi.

**Project1.exe:** programa compilado para Windows.

**bandeiras.bin:** dados auxiliares utilizados na restauração das bandeiras.

**Background/:** imagens utilizadas no desenvolvimento visual.

**Imagens/:** arquivos gráficos relacionados às equipes.

**Arquivos de offsets:** documentação técnica sobre endereços e valores binários de jogos da série.

## Como utilizar

1. Execute `Project1.exe` no Windows.
2. Clique em **ISO** e selecione o arquivo BIN do jogo.
3. Acesse a seção desejada do editor.
4. Escolha as configurações ou equipes que deseja modificar.
5. A ferramenta aplica as alterações no arquivo selecionado.
6. Utilize as opções de restauração disponíveis quando necessário.

## Informações importantes

- Faça backup do BIN original antes de realizar qualquer modificação.
- O programa altera diretamente o arquivo selecionado.
- Algumas modificações dependem de offsets específicos da versão do jogo.
- Mantenha o arquivo `bandeiras.bin` junto ao executável.
- As configurações de velocidade Turbo e o limite ampliado de contratações podem produzir comportamentos diferentes dos encontrados no jogo original.
- O software é uma versão experimental e pode apresentar limitações.

## Créditos

**Programação e desenvolvimento:** Fabio FJA

**Pesquisa de offsets:** Fabio FJA / Polipoli

**Referência para o editor de equipes:** Team Remover by Cuervo

**Versão:** 0.1

**Linguagem:** Object Pascal / Delphi

**Plataforma do jogo:** PlayStation 1

Projeto independente desenvolvido para estudo, pesquisa, engenharia reversa e personalização de jogos clássicos de futebol.

Este projeto não possui vínculo oficial com a Konami.
