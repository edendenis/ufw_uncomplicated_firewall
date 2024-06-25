# Como instalar/configurar para o `UFW (Uncomplicated Firewall)` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para instalar/configurar o `UFW (Uncomplicated Firewall)` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings to install/configure the `UFW (UNcomplicated Firewall)` on `Linux Ubuntu`._

## Descrição

O `UFW (Uncomplicated Firewall)` é uma interface de usuário para o sistema de firewall iptables do `Linux`, projetada para tornar a gestão de regras de firewall mais simples e acessível. Ele permite que usuários, mesmo aqueles com conhecimento limitado em segurança de rede, configurem regras de firewall de maneira fácil e intuitiva, oferecendo um método direto para habilitar ou desabilitar o tráfego de rede em sistemas `Ubuntu` e outras distribuições `Linux` baseadas no Debian.


## 1. Instalar o `UFW (Uncomplicated Firewall)` no `Linux Ubuntu` (caso ainda não esteja instalado) [1]

Para ativar o firewall no `Ubuntu 22.04 LTS`, você pode usar o `UFW (Uncomplicated Firewall)`, que é uma interface mais amigável para gerenciar o iptables, o sistema de firewall do `Linux`. Siga as etapas abaixo:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`


2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update`

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes: `sudo apt --fix-broken install`

    2.6 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`
    

3. Instale o UFW com o comando: `sudo apt install ufw -y`

4. **Ativar o UFW:** Para ativar o UFW, execute o comando: `sudo ufw enable`

5. **Verificar o status do UFW**: Você pode verificar o status do UFW a qualquer momento usando: `sudo ufw status`

Aqui estão os comandos correspondentes para cada etapa:

## 1.1 Comentários sobre os comandos

- **`sudo apt update`:** Este comando atualiza a lista de pacotes disponíveis para instalação.
- **`sudo apt install ufw`:** Este comando instala o pacote UFW.
- **`sudo ufw enable`:** Este comando ativa o firewall UFW.
- **`sudo ufw status`:** Este comando mostra o status atual do firewall, incluindo quais portas estão abertas e quais regras estão ativas.

Depois de ativar o UFW, você pode começar a adicionar regras para permitir ou bloquear tráfego específico, conforme necessário.

## 2. Código completo

Para instalar o `ufw` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt clean                                                            ─╯
    sudo apt autoclean
    sudo apt autoremove -y
    sudo apt update
    sudo apt --fix-broken install
    sudo apt clean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo apt install ufw -y
    sudo ufw enable
    sudo ufw status
    ```

## Referências

[1] OPENAI. ***Ativar Firewall no Ubuntu.*** Disponível em: <https://chat.openai.com/c/ccab59aa-3e70-465e-906d-59d7038ea632> (texto adaptado). Acessado em: 30/10/2023 11:11.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). ChatGPT. Acessado em: 30/10/2023 13:51.

