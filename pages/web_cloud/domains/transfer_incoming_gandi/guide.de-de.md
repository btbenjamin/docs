---
title: "Gandi-Domainnamen zu OVHcloud transferieren"
excerpt: "Erfahren Sie hier, wie Sie einen Gandi-Domainnamen zu OVHcloud transferieren"
updated: 2024-06-28
---

## Ziel

Für den Transfer eines Gandi-Domainnamens ist ein spezieller Ansatz erforderlich.

> [!warning]
>
> Der [Domainnamen-Registrar](/links/web/domains-what-is-registrar) ist ein Diensteanbieter, der authorisiert ist, Domainnamen zur Registrierung seitens Privatpersonen, Unternehmen oder sonstigen Organisationen anzubieten. Sie verlängern ein Domainnamen-Abonnement bei Ihrem Registrar, üblicherweise jährlich.
>
> Wenn OVHcloud bereits der Registrar Ihres Domainnamens ist, ist der Prozess des eingehenden Transfers nicht für diesen Domainnamen anwendbar. Das in dieser Anleitung beschriebene Verfahren für eingehende Domaintransfers gilt **nur** für Domainnamen, die derzeit bei einem anderen Registrar als OVHcloud registriert sind.
>
> Um die Verwaltung des Domainnamens einem anderen OVHcloud Kunden-Account zu übertragen, muss stattdessen eine **Änderung der Kontakte** durchgeführt werden. Die Vorgehensweise wird in [unserer Anleitung zur Kontakteverwaltung](/pages/account_and_service_management/account_information/managing_contacts) beschrieben.
>
> Wenn auch der **Inhaber des Domainnamens** geändert werden muss, sollte dies erfolgen, **bevor** Sie die Kontakte des Domainnamens ändern. Verwenden Sie dazu [unsere Anleitung zum Inhaberwechsel für Domainnamen](/pages/web_cloud/domains/trade_domain).
>

**Diese Anleitung erklärt, wie Sie einen Gandi-Domainnamen zu OVHcloud transferieren.**

> [!warning]
>
> Der Gandimail-Dienst ist mit Ihrem Domainnamen verbunden. Er wird nicht mehr funktionieren, sobald der Domainname von Gandi transferiert wird. 
>
> E-Mail-Accounts, die mit diesem Domainnamen verbunden sind, werden 7 Tage später endgültig gelöscht, **einschließlich des gesamten Inhalts**.
>
> Es ist daher wichtig, dass Sie Ihre Inhalte sichern, bevor Sie mit dem Transfer des Domainnamens beginnen.
>

## Voraussetzungen

- Sie verfügen über einen Domainnamen bei Gandi.
- Der Domainname existiert seit mehr als 60 Tagen.
- Der Domainname wurde in den letzten 60 Tagen nicht transferiert und der Inhaber wurde nicht geändert.
- Der Zustand des Domainnamens ist "OK" oder "Transferable".
- Der Domainname ist nicht abgelaufen und hat ein Ablaufdatum, das den Transfer noch ermöglicht (empfohlen sind mehr als 60 Tage).
- Sie können den Domainnamen entsperren und Sie haben bereits den Transfer-Code oder können ihn anfordern.
- Sie besitzen die Verfügungsberechtigung, um den Transfer des Domainnamens zu veranlassen.
- Der Domaininhaber und/oder dessen Administratoren sind über den Transfer informiert.

> [!warning]
> OVHcloud stellt Ihnen Dienstleistungen zur Verfügung, für deren Konfiguration und Verwaltung Sie die alleinige Verantwortung tragen. Es liegt somit bei Ihnen, sicherzustellen, dass diese ordnungsgemäß funktionieren.
> 
> Diese Anleitung soll Sie bei allgemeinen Aufgaben bestmöglich unterstützen. Dennoch empfehlen wir Ihnen, falls Sie Hilfe brauchen, einen [spezialisierten Dienstleister](/links/partner) zu kontaktieren oder Ihren aktuellen Registrar zu kontaktieren. Leider können wir Ihnen für externe Dienstleistungen keine weitergehende Unterstützung anbieten. Weitere Informationen finden Sie am [Ende dieser Anleitung](#go-further).
>

## In der praktischen Anwendung

> [!primary]
>
> Die aktive DNS-Zone eines Domainnamens enthält die auf Ihre Domainnamen angewendete DNS-Konfiguration. Sie verbindet Ihren Domainnamen mit Ihren Diensten wie E-Mail-Adressen oder Ihrer Website.
>
> Wenn Sie zusätzlich zu Ihrem Domainnamen bei Ihrem aktuellen Registrar über eine aktive DNS-Zone verfügen, vergewissern Sie sich, dass die auf Ihren Domainnamen angewendete DNS-Zone nach dem Transfer nicht gelöscht wird.
>
> Einige Registrare löschen die DNS-Zone, sobald der Transfer Ihres Domainnamens abgeschlossen ist. Ist das der Fall, erstellen Sie Ihre DNS-Zone bei OVHcloud neu, bevor Sie mit den Aktionen zum Transfer Ihres Domainnamens beginnen.
>
> Lesen Sie hierzu die folgenden Anleitungen:
>
> - [DNS-Zone bei OVHcloud erstellen](/pages/web_cloud/domains/dns_zone_create)
> - [OVHcloud DNS-Zone bearbeiten](/pages/web_cloud/domains/dns_zone_edit)
>
> Stellen Sie außerdem sicher, dass Ihr aktueller Registrar nicht andere Dienste abstellt, z.B. die E-Mail-Adressen, die mit Ihrem Domainnamen verknüpft sind.
>
> Wenn Sie neben dem Transfer Ihrer Domain auch die dazugehörigen Dienste (Website, E-Mail, etc.) migrieren möchten, lesen Sie zuerst unsere Anleitung „[Website und dazugehörige Dienste zu OVHcloud migrieren](/pages/web_cloud/web_hosting/hosting_migrating_to_ovh)“, bevor Sie fortfahren.
> In dieser Anleitung erfahren Sie, wie Sie alle Ihre Dienstleistungen ohne Unterbrechung migrieren.
>
> Wenn Sie Ihren Domainnamen nur transferieren, ohne Ihre anderen Dienste zu verlegen, stellen Sie sicher, dass Sie die aktiven DNS-Server für Ihren Domainnamen von Ihrem **aktuellen Registrar** erfahren, um diese direkt in Schritt 3 der Anleitung „[Domainnamen zu OVHcloud transferieren](/pages/web_cloud/domains/transfer_incoming_generic_domain)“ einzugeben.
> So wird vermieden, dass die Zuordnung zwischen Ihrem Domainnamen und den zugehörigen externen Diensten unterbrochen wird.
>

### Schritt 1 - Transfer-Sperre deaktivieren

> [!warning]
>
> Die meisten Domainendungen verfügen über eine Sperrfunktion gegen den Transfer, die im [Whois](/links/web/domains-whois) als „transferProhibited“ bezeichnet ist.
>
> Diese Sperrung verhindert unbeabsichtigtes Übertragen.
>
> Solange die Sperre aktiv ist, ist die Übertragung nicht möglich.
>

Um Ihren Domainnamen bei Gandi zu entsperren, folgen Sie den Schritten in der [Gandi Dokumentation](https://docs.gandi.net/en/domain_names/transfer_out/transfer_lock.html){.external}.

### Schritt 2 - Autorisierungscode abrufen

Der Autorisierungscode schützt Ihren Domainnamen gegen unbefugte Transfers durch Dritte. Dieser Code ist erforderlich, um den Transfer Ihres Domainnamens zu einem neuen Registrar zu autorisieren.

Um den Transfer-Code für Ihren Domainnamen abzurufen, folgen Sie den Schritten in der [Gandi Dokumentation](https://docs.gandi.net/en/domain_names/transfer_out/auth_info.html){.external}.

### Schritt 3 - Transfer Ihres Domainnamens zu OVHcloud einleiten
  
Sobald Sie den Autorisierungscode erhalten haben, können Sie den Transfer Ihres Domainnamens durchführen, indem Sie die Schritte in unserer Anleitung "[Domainnamen zu OVHcloud transferieren](/pages/web_cloud/domains/transfer_incoming_generic_domain)" befolgen.

> [!warning]
>
> Innerhalb von 24 Stunden nach Beginn des Transfers wird Gandi Ihnen eine E-Mail mit einer Benachrichtigung zusenden, um Sie über die Freigabe des Domainnamens zu informieren.
> Diese E-Mail kann auch einen Link enthalten, über den Sie den Transfer anstelle von Gandi akzeptieren können, was die Reservierungsfrist verkürzt.
> Die Reservierungsfrist beträgt 5 Tage (8 Tage für von AFNIC verwaltete Domainnamen) und erlaubt es, den Transfer zu stornieren.
> Nach Ablauf dieser Frist (5 Tage) wird der Transfer automatisch abgeschlossen.
>

## Weiterführende Informationen <a name="go-further"></a>

[Website und E-Mails zu OVHcloud migrieren](/pages/web_cloud/web_hosting/hosting_migrating_to_ovh)
 
Kontaktieren Sie für spezialisierte Dienstleistungen (SEO, Web-Entwicklung etc.) die [OVHcloud Partner](/links/partner).
 
Wenn Sie Hilfe bei der Nutzung und Konfiguration Ihrer OVHcloud Lösungen benötigen, beachten Sie unsere [Support-Angebote](/links/support).
 
Treten Sie unserer [User Community](/links/community) bei.
