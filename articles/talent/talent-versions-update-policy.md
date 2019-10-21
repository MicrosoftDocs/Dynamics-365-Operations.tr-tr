---
title: Talent sistem gereksinimleri ve güncelleştirme ilkesi
description: Bu konu Dynamics 365 Talent için gereksinimleri listeler. Güncelleştirme ilkesi de açıklanmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b8bf44fc76be968b0b04fd894c39b4c19fd374ce
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024172"
---
# <a name="talent-system-requirements-and-update-policy"></a>Talent sistem gereksinimleri ve güncelleştirme ilkesi

[!include [banner](includes/banner.md)]

Bu konu Attract, Onboard ve Core HR dahil olmak üzere Microsoft Dynamics 365 Talent için gereksinimleri açıklar. Ayrıca, Talent'ın kullanılabildiği ülkeler ve bölgeler ile birlikte Talent verileri için diller ve yerelleştirme hakkında bilgiler de ana hatlarıyla açıklanmıştır. Ek olarak bu konu Talent ile ilgili güncelleştirme ilkesini içerir.

## <a name="supported-web-browsers"></a>Desteklenen web tarayıcıları

Microsoft Dynamics 365 Talent belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarından herhangi birinde çalışabilir: 

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
> * Dynamics 365 Talent 250-300 milisaniye (ms) veya daha az gecikmeye sahip ağlar için tasarlanmıştır. Bu, bir tarayıcı istemcisinden Talent'ı barındıran Microsoft Azure veri merkezine iletim süresidir. Ağ gecikmesini [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test") adresinden test etmenizi öneririz.
> * Talent için bant genişliği gereksinimlerini senaryoya bağlıdır. En tipik senaryolar 50 kilobayt/saniye (KBps) üzerinde bir bant genişliği gerektirir.
> 
> [!WARNING]
> Kullanıcı sayısıyla minimum bant genişliği gereksinimlerini çarpıp bir müşteri konumundan bant genişliği gereksinimlerini hesaplamayın. Belirli bir konumun eşzamanlı kullanımını hesaplamak çok zordur. Bant genişliği gereksinimleri konusunda kaygıları olan müşteriler Talent'ın bir deneme sürümünü kullanabilir.

## <a name="supported-microsoft-office-applications"></a>Desteklenen Microsoft Office uygulamaları

* Microsoft Excel ve Word eklentilerini çalıştırmak için Windows veya Mac için Microsoft Office 2016'yı yüklemiş olmanız gerekir. Sürüm gereksinimleri hakkında daha fazla bilgi için bkz. [Office tümleştirme sorunlarını giderme](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office tümleştirme sorunlarını giderme").
* Excel'e Aktar veya Word'e Aktar işleviyle oluşturulan belgeleri görüntülemek için Microsoft Office 2007 veya sonraki bir sürümü yüklemiş olmanız gerekir.

## <a name="regional-availability-languages-and-localization"></a>Bölgesel kullanılabilirlik, diller ve yerelleştirme

Talent'ın desteklediği ülkeler, bölgeler ve dillere ilişkin bir PDF dosyasını [Microsoft Dynamics 365'in uluslararası kullanılabilirliği](https://docs.microsoft.com/dynamics365/get-started/availability) bölümünden indirebilirsiniz. 

> [!NOTE]
> Kullanıcı arabirimi başka dillere yerelleştirilmiş olmasına karşın, tüm kullanıcı verileri girildiği dilde depolanır. Diğer dillerde e-postalar ve şablonlar oluşturabilirsiniz ancak zamanlama bilgileri gibi veriler şu anda yalnızca İngilizce olarak kullanılabilir.

Ülkeye veya bölgeye özel özelleştirmeler oluşturmakla ilgilenen bir geliştiricisiyseniz veya şu anda Microsoft tarafından desteklenmeyen bir ülke veya bölge için çözüm oluşturan bir geliştiriciyseniz bkz. [Globalleştirme](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).

## <a name="update-policy"></a>Güncelleştirme ilkesi

Talent bir bulut hizmeti olarak sunulmaktadır. Talent güncelleştirmeleri süreklidir ve Microsoft tarafından otomatik olarak uygulanır.

Güncelleştirmeler düzenli aralıklarla yayımlanır ve tüm ortamlar için yapılır. Talent, ürün destek kullanılabilirliği hakkında düzenli ve öngörülebilir kılavuzlar sunan [Microsoft Desteği Yaşam Döngüsü ilkesine](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Desteği Yaşam Döngüsü") uygun olarak desteklenir.
