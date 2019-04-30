---
title: Talent sistem gereksinimleri ve güncelleştirme ilkesi
description: Bu konu Dynamics 365 for Talent için gereksinimleri listeler. Güncelleştirme ilkesi de açıklanmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
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
ms.openlocfilehash: 2389f00b22ec3b5284eeffb2c015533b7a3d13e0
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "856313"
---
# <a name="talent-system-requirements-and-update-policy"></a>Talent sistem gereksinimleri ve güncelleştirme ilkesi

[!include [banner](includes/banner.md)]

Bu konu Microsoft Dynamics 365 for Talent için gereksinimleri listeler. Güncelleştirme ilkesi de açıklanmaktadır.

## <a name="supported-web-browsers"></a>Desteklenen web tarayıcıları

Microsoft Dynamics 365 for Talent web uygulamasını belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarından birinde çalıştırabilirsiniz: 

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
> * Dynamics 365 for Talent 250-300 milisaniye (ms) veya daha az gecikmeye sahip ağlar için tasarlanmıştır. Bu, bir tarayıcı istemcisinden Dynamics 365 for Talent'ı barındıran Microsoft Azure veri merkezine iletim süresidir. Ağ gecikmesini [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test") adresinden test etmenizi öneririz.
> * Dynamics 365 for Talent için bant genişliği gereksinimlerini senaryoya bağlıdır. En tipik senaryolar 50 kilobayt/saniye (KBps) üzerinde bir bant genişliği gerektirir.
> 
> [!WARNING]
> Kullanıcı sayısıyla minimum bant genişliği gereksinimlerini çarpıp bir müşteri konumundan bant genişliği gereksinimlerini hesaplamayın. Belirli bir konumun eşzamanlı kullanımını hesaplamak çok zordur. Bant genişliği gereksinimleri konusunda kaygıları olan müşteriler Dynamics 365 for Talent'ın bir deneme sürümünü kullanabilir.

## <a name="supported-microsoft-office-applications"></a>Desteklenen Microsoft Office uygulamaları

* Microsoft Excel ve Word eklentilerini çalıştırmak için Windows veya Mac için Microsoft Office 2016'yı yüklemiş olmanız gerekir. Sürüm gereksinimleri hakkında daha fazla bilgi için bkz. [Office tümleştirme sorunlarını giderme](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office tümleştirme sorunlarını giderme").
* Excel'e Aktar veya Word'e Aktar işleviyle oluşturulan belgeleri görüntülemek için Microsoft Office 2007 veya sonraki bir sürümü yüklemiş olmanız gerekir.

## <a name="update-policy"></a>Güncelleştirme ilkesi

Microsoft Dynamics 365 for Talent, bir bulut hizmeti olarak sunulur. Dynamics 365 for Talent güncelleştirmeleri süreklidir ve Microsoft tarafından otomatik olarak uygulanır.

Güncelleştirmeler düzenli aralıklarla yayımlanır ve güncelleştirmeler tüm ortamlar için yapılır.  Dynamics 365 for Talent, ürün destek kullanılabilirliği hakkında düzenli ve öngörülebilir kılavuzlar sunan [Microsoft Desteği Yaşam Döngüsü ilkesi](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Desteği Yaşam Döngüsü") ile uygun olarak desteklenir.
