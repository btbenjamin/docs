---
title: 'Exchange - Configure sua conta de e-mail no Thunderbird para macOS'
excerpt: 'Encontre aqui o procedimento para adicionar uma conta Exchange para Thunderbird'
updated: 2024-10-09
---

## Objetivo

As contas Exchange podem ser configuradas em vários softwares de e-mail compatíveis. Isto permite-lhe usar o seu endereço de e-mail no dispositivo que preferir. A Thunderbird é um cliente de e-mails livre e gratuito.

**Saiba como configurar o seu endereço de Exchange no Thunderbird no Windows.**

> [!warning]
>
> A responsabilidade sobre a configuração e a gestão dos serviços que a OVHcloud disponibiliza recai sobre o utilizador. Assim, deverá certificar-se de que estes funcionam corretamente.
> 
> Este manual fornece as instruções necessárias para realizar as operações mais habituais. No entanto, se encontrar dificuldades, recomendamos que recorra a um [prestador de serviços especializado](/links/partner) e/ou que contacte o editor do serviço. Não poderemos proporcionar-lhe assistência técnica. Para mais informações, aceda à secção «Quer saber mais?» deste guia.
> 

## Requisitos

- Ter um endereço de [Exchange](/links/web/emails-hosted-exchange).
- Dispor do software Thunderbird instalado no seu Windows.
- Dispor das credenciais do endereço de e-mail que pretende configurar.
 
## Instruções

> [!warning]
>
> No nosso exemplo, utilizamos a menção servidor: ex**?**.mail.ovh.net. Deverá substituir o "? " pelo número que designa o servidor do seu serviço Exchange.
> 
> Encontre este número na sua [Área de Cliente OVHcloud](/links/manager), na rubrica `Web Cloud`{.action} e depois `Microsoft`{.action}/`Exchange`{.action}. O servidor é visível na secção **Ligação** do separador `Informações gerais`{.action}.
> 

### Adicionar a conta

- **Se for a primeira vez que utiliza a aplicação**, aparecerá um assistente de configuração que lhe irá solicitar o seu endereço de e-mail.

- **Se uma conta já estiver configurada**: clique em `Ficheiro`{.action} na barra de menu no topo do seu ecrã, depois em `Novo`{.action} e, por fim, em `Obter uma nova conta de correio...`{.action}.

| | |
|---|---|
|![Thunderbird](images/thunderbird-win-exchange01.png){.thumbnail}|Na nova janela, introduza as seguintes 3 informações: <br>- O seu nome completo (Nome de apresentação)<br>- Endereço eletrónico <br>- Palavra-passe.|
|A seguir, clique em `Configurar manualmente...`{.action} para introduzir os parâmetros do servidor **ENTRAANT**: <br>- Protocolo **IMAP** <br>- Servidor **ex?.mail.ovh.net** <br>- Porta **993** <br>- SSL **SSL/TLS** <br>- Autenticação da **password normal** <br>- Identificar **o seu endereço de e-mail completo**|![Thunderbird](images/thunderbird-win-exchange02.png){.thumbnail}|
|![Thunderbird](images/thunderbird-win-exchange03.png){.thumbnail}|Introduzir os parâmetros do servidor de **saída**: <br>- Protocolo **SMTP** <br>- Servidor **ex?.mail.ovh.net** <br>- Porta **587** <br>- SSL **STARTTLS** <br>- Autenticação da **password normal** <br>- Identificar **o seu endereço de e-mail completo**<br><br>Para terminar a configuração, clique em `Terminado`{.action}|

No âmbito de uma configuração em **POP**, os valores são os seguintes:

|Tipo de servidor|Nome do servidor|Método de encriptação|Porta|
|---|---|---|---|
|De entrada|ex**?**.mail.ovh.net (a menção **"?"** é substituída pelo número do seu servidor)|SSL/TLS|995|
|De saída|ex**?**.mail.ovh.net (a menção **"?"** é substituída pelo número do seu servidor)|STARTTLS|587|

### Utilizar o endereço de e-mail

Após a configuração, a conta de e-mail está pronta a usar e pode começar a enviar e receber mensagens no seu dispositivo.

A OVHcloud também disponibiliza uma aplicação web que permite aceder ao seu endereço de e-mail a partir de um browser. disponível no endereço [Webmail](/links/web/email). Para aceder, só precisa dos dados de acesso do seu endereço de e-mail. Para qualquer questão relativa à sua utilização, consulte o nosso manual [Consultar a sua conta Exchange a partir da interface OWA](/pages/web_cloud/email_and_collaborative_solutions/using_the_outlook_web_app_webmail/email_owa).

### Recuperar um backup do seu endereço de e-mail

Se tiver de efetuar uma operação suscetível de causar a perda dos dados da sua conta de e-mail, sugerimos que efetue uma cópia de segurança da conta de e-mail em questão. Para isso, consulte o parágrafo "**Exportar**" na secção "**Thunderbird**" do nosso guia [Migrar manualmente o seu endereço de e-mail](/pages/web_cloud/email_and_collaborative_solutions/migrating/manual_email_migration).

### Modificar os parâmetros existentes

> [!warning]
>
> No nosso exemplo, utilizamos a menção servidor: ex**?**.mail.ovh.net. Deverá substituir o "? " pelo número que designa o servidor do seu serviço Exchange.
> 
> Encontre este número na sua [Área de Cliente OVHcloud](/links/manager), na rubrica `Web Cloud`{.action} e depois `Microsoft`{.action}/`Exchange`{.action}. O servidor é visível na secção **Ligação** do separador `Informações gerais`{.action}.
> 

Se a sua conta de e-mail já está configurada e tem de aceder aos parâmetros da conta para os alterar:

- Aceda às `Ferramentas`{.action} a partir da barra de menu no topo do ecrã.
- Clique em `Parâmetros das contas`{.action}.

![Thunderbird](images/thunderbird-win-exchange04.png){.thumbnail}

- Para alterar os parâmetros associados à **receção** dos seus e-mails, clique em `Parâmetros do servidor`{.action} na coluna da esquerda do seu endereço de e-mail.

![Thunderbird](images/thunderbird-win-exchange05.png){.thumbnail}

- Para modificar os parâmetros associados ao **envio**dos seus e-mails, clique em `Servidor de saída (SMTP)`{.action} no fundo da coluna da esquerda.
- Clique no endereço de e-mail em questão na lista e, a seguir, em `Alterar`{.action}.

![Thunderbird](images/thunderbird-win-exchange06.png){.thumbnail}

## Saiba mais

> [!primary]
>
> Para obter mais informações sobre a configuração de um endereço de e-mail a partir da aplicação Thunderbird no Windows, consulte [Central de Ajuda do Mozilla](https://support.mozilla.org/pt-BR/kb/configuracao-manual-de-conta#thunderbird:win10:tb115).

Fale com a nossa comunidade de utilizadores em <https://community.ovh.com/en/>.