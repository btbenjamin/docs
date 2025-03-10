---
title: 'Exchange - Skonfiguruj swoje konto e-mail w programie Outlook dla systemu Windows'
excerpt: 'Dowiedz się, jak skonfigurować konto Exchange w programie Outlook na urządzeniu z systemem Windows'
updated: 2024-10-30
---

## Wprowadzenie

Konta Exchange mogą być skonfigurowane w jednym z kompatybilnych programów pocztowych.  Dzięki temu możesz używać Twojego konta e-mail, korzystając z wybranej przez Ciebie aplikacji. Microsoft Outlook jest aplikacją zalecaną do korzystania z konta e-mail Exchange ze swoimi funkcjami współpracy.

**Dowiedz się, jak skonfigurować konto Exchange w programie Microsoft Outlook na urządzeniu z systemem Windows.**

> [!warning]
>
> OVHcloud udostępnia różnorodne usługi, jednak to Ty odpowiadasz za ich konfigurację i zarządzanie nimi. Ponosisz więc odpowiedzialność za ich prawidłowe funkcjonowanie.
> 
> Oddajemy w Twoje ręce niniejszy przewodnik, którego celem jest pomoc w wykonywaniu bieżących zadań. W przypadku trudności zalecamy skorzystanie z pomocy wyspecjalizowanego webmastera lub kontakt z producentem oprogramowania. Niestety firma OVHcloud nie będzie mogła udzielić wsparcia w tym zakresie. Więcej informacji znajduje się w sekcji „Sprawdź również”.
> 

<iframe class="video" width="560" height="315" src="https://www.youtube-nocookie.com/embed/2YeGXo10CX8?si=mINBBXq6qb4MiFEt" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Wymagania początkowe

- Wykupienie usługi [Exchange](/links/web/emails).
- Instalacja programu Microsoft Outlook lub nowszego oprogramowania na Twoim komputerze
- Dane do logowania do konta e-mail, które chcesz skonfigurować
- Pole SRV OVHcloud musi być poprawnie skonfigurowane w strefie DNS domeny. Sprawdź nasz przewodnik [Dodaj domenę do usługi Exchange](/pages/web_cloud/email_and_collaborative_solutions/microsoft_exchange/exchange_adding_domain).

> [!primary]
>
> Używasz programu Outlook i później na urządzeniu Mac? Zapoznaj się z naszą dokumentacją: [Konfiguracja konta Exchange w programie Outlook na urządzeniu Mac](/pages/web_cloud/email_and_collaborative_solutions/microsoft_exchange/how_to_configure_outlook_2016_mac).

## W praktyce

### Dodaj konto

- **Podczas pierwszego uruchomienia aplikacji**: wyświetli się asystent konfiguracji i poprosi o wpisanie adresu e-mail.

- **Jeżeli inne konto zostało wcześniej skonfigurowane**: kliknij `Plik`{.action} na pasku menu na górze Twojego ekranu, a następnie kliknij `Dodaj konto`{.action}.

- Wpisz hasło dla Twojego konta e-mail, po czym kliknij `Dalej`{.action}. Zaznacz kratkę obok komunikatu `Pozwól mi ręcznie skonfigurować moje konto `{.action}, a następnie kliknij `Połącz`{.action}. 

![Exchange](images/config-outlook-exchange01.png){.thumbnail}

- Spośród różnych rodzajów kont wybierz **Exchange**.

- Wpisz hasło przypisane do Twojego konta e-mail w kolejnym oknie, zaznacz kratkę, aby je zapamiętać, następnie kliknij `OK`{.action}.

![Exchange](images/config-outlook-exchange02.png){.thumbnail}

> [!primary]
> 
> Jeśli pojawi się komunikat, że Outlook nie mógł skonfigurować Twojego konta, może to oznaczać, że pole SRV OVHcloud nie jest poprawnie skonfigurowane w strefie DNS Twojej domeny.
> 
> ![Exchange](images/config-outlook-exchange03.png){.thumbnail}
>
> Zalecamy sprawdzenie konfiguracji domeny w Twojej usłudze Exchange w [Panelu klienta OVHcloud](/links/manager), w zakładce `Powiązane domeny `{.action}, a następnie w kolumnie `Diagnostyka`{.action} w tabeli.

- Jeśli konfiguracja Twojej domeny jest prawidłowa, może pojawić się komunikat o autoryzacji połączenia z serwerami OVHcloud. Zaakceptuj to, aby umożliwić automatyczną konfigurację konta Exchange.
- Następnie określ częstotliwość przechowywania danych na koncie Exchange, dostępna **lokalnie na komputerze**. Kliknij `Dalej`{.action}, a następnie `Zakończ`{.action}.

![Exchange](images/config-outlook-exchange04.png){.thumbnail}

### Użyj konta e-mail

Po zakończeniu konfiguracji konto jest gotowe do użytku. Możesz teraz zacząć wysyłać i odbierać wiadomości.

Twój adres e-mail Exchange oraz wszystkie jego funkcje do pracy zespołowej są również dostępne w interfejsie [OWA](/links/web/email). W przypadku pytań dotyczących korzystania z tego konta, zapoznaj się z naszym przewodnikiem [Sprawdź konto Exchange w interfejsie OWA](/pages/web_cloud/email_and_collaborative_solutions/using_the_outlook_web_app_webmail/email_owa).

### Pobierz kopię zapasową Twojego konta e-mail

Jeśli musisz wykonać operację, która może spowodować utratę danych przypisanych do Twojego konta e-mail, zalecamy wykonanie kopii zapasowej odpowiedniego konta e-mail. W tym celu zapoznaj się z sekcją "**Eksport z systemu Windows**" w przewodniku [Ręczna migracja Twojego konta e-mail](/pages/web_cloud/email_and_collaborative_solutions/migrating/manual_email_migration#eksport-z-systemu-windows).

## Sprawdź również

> [!primary]
>
> Aby uzyskać więcej informacji na temat konfigurowania konta e-mail z poziomu aplikacji Outlook na urządzeniach z systemem Windows, zobacz [Centrum pomocy Microsoft](https://support.microsoft.com/pl-pl/office/dodawanie-konta-e-mail-do-programu-outlook-6e27792a-9267-4aa4-8bb6-c84ef146101b).

[Konfiguracja konta e-mail, zawartego w usłudze MX Plan lub usłudze hostingu, w programie Outlook na urządzeniu z systemem Windows](/pages/web_cloud/email_and_collaborative_solutions/mx_plan/how_to_configure_outlook_2016).

[Konfiguracja konta E-mail Pro w programie Outlook na urządzeniu z systemem Windows](/pages/web_cloud/email_and_collaborative_solutions/email_pro/how_to_configure_outlook_2016)

Dołącz do społeczności naszych użytkowników na stronie <https://community.ovh.com/en/>.
