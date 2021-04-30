---
title: Sistem gereksinimleri
description: Bu makalede, Microsoft Dynamics 365 Human Resources ile ilgili gereksinimler anlatılmaktadır.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a4266ee942f504ffa2f355959af8e3076984d83
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892311"
---
# <a name="system-requirements"></a>Sistem gereksinimleri

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Microsoft Dynamics 365 Human Resources ile ilgili gereksinimler anlatılmaktadır. Ayrıca, İnsan Kaynaklarının kullanılabildiği ülkeler ve bölgeler ile birlikte İnsan Kaynakları verileri için diller ve yerelleştirme hakkında bilgiler de ana hatlarıyla açıklanmıştır.

## <a name="supported-web-browsers"></a>Desteklenen web tarayıcıları

İnsan Kaynakları belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarından herhangi birinde çalışabilir: 

*   Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)
*   Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
*   Google Chrome (genel yayımlanmış en son sürüm)
*   Apple Safari (genel yayımlanmış son sürüm)

Her web tarayıcısı için en son sürümü bulmak için, yazılım üreticisinin web sitesine gidin. 

> [!NOTE]
> * Görev Kaydedici'den oluşturulmuş görüntüleri yakalamak ve bunları Microsoft Word belgelerine eklemek için bir Chrome eklentisinin yüklü olması gerekir. 
> * İş Akışı Düzenleyicisi bir ClickOnce uygulaması olarak başlatılır. Yalnızca Microsoft Edge ve Internet Explorer (desteklenen bir Microsoft Windows sürümü üzerinde) ClickOnce uygulamalarını destekler. İş Akışı Düzenleyicisi ClickOnce uygulaması için 64-bit uyumlu bir işletim sistemi gereklidir.
> * PDF dosyalarının önizlemesini yapmak için (en son sürüm genel kullanıma açık) Windows 10 üzerinde, Microsoft Edge veya (en son sürüm genel kullanıma açık) Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome gibi modern tarayıcıları kullanmanızı öneririz.
>   Ağ gereksinimleri
> * İnsan Kaynakları 250-300 milisaniye (ms) veya daha az gecikmeye sahip ağlar için tasarlanmıştır. Bu, bir tarayıcı istemcisinden İnsan Kaynakları'nı barındıran Microsoft Azure veri merkezine iletim süresidir. Ağ gecikmesini [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test") adresinde sınamanızı öneririz.
> * İnsan Kaynakları için bant genişliği gereksinimlerini senaryoya bağlıdır. En tipik senaryolar 50 kilobayt/saniye (KBps) üzerinde bir bant genişliği gerektirir.
> 
> [!WARNING]
> Kullanıcı sayısıyla minimum bant genişliği gereksinimlerini çarpıp bir müşteri konumundan bant genişliği gereksinimlerini hesaplamayın. Belirli bir konumun eşzamanlı kullanımını hesaplamak çok zordur. Bant genişliği gereksinimleri konusunda kaygıları olan müşteriler İnsan Kaynakları'nın bir deneme sürümünü kullanabilir.

## <a name="supported-microsoft-office-applications"></a>Desteklenen Microsoft Office uygulamaları

* Microsoft Excel ve Word eklentilerini çalıştırmak için Windows veya Mac için Microsoft Office 2016'yı yüklemiş olmanız gerekir. Sürüm gereksinimleri hakkında daha fazla bilgi için bkz. [Office tümleştirme sorunlarını giderme](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Office tümleştirme sorunlarını giderme").
* Excel'e Aktar veya Word'e Aktar işleviyle oluşturulan belgeleri görüntülemek için Microsoft Office 2007 veya sonraki bir sürümü yüklemiş olmanız gerekir.

## <a name="regional-availability-languages-and-localization"></a>Bölgesel kullanılabilirlik, diller ve yerelleştirme

İnsan Kaynakları'nın desteklediği ülkeler, bölgeler ve dillere ilişkin bir PDF dosyasını [Microsoft Dynamics 365'in uluslararası kullanılabilirliği](/dynamics365/get-started/availability) bölümünden indirebilirsiniz. 

> [!NOTE]
> Kullanıcı arabirimi başka dillere yerelleştirilmiş olmasına karşın, tüm kullanıcı verileri girildiği dilde depolanır. Diğer dillerde e-postalar ve şablonlar oluşturabilirsiniz ancak zamanlama bilgileri gibi veriler şu anda yalnızca İngilizce olarak kullanılabilir.

Ülkeye veya bölgeye özel özelleştirmeler oluşturmakla ilgilenen bir geliştiricisiyseniz veya şu anda Microsoft tarafından desteklenmeyen bir ülke veya bölge için çözüm oluşturan bir geliştiriciyseniz bkz. [Globalleştirme](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).


[!INCLUDE[footer-include](../includes/footer-banner.md)]