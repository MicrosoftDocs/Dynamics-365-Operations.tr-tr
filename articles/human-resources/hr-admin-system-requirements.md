---
title: Sistem gereksinimleri
description: Bu konuda, Microsoft Dynamics 365 Human Resources için sistem gereksinimleri listelenmektedir.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15770595a0639c03df1138ec25010ca8168bd9a8
ms.sourcegitcommit: 49f7528d3268abe15e40f719956e1ec8696a6f4e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/18/2021
ms.locfileid: "7393485"
---
# <a name="system-requirements"></a>Sistem gereksinimleri

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Microsoft Dynamics 365 Human Resources için sistem gereksinimleri listelenmektedir. Ayrıca, İnsan Kaynaklarının kullanılabildiği ülkeler ve bölgeler ile birlikte İnsan Kaynakları verileri için diller ve yerelleştirme hakkında bilgiler de ana hatlarıyla açıklanmıştır.

## <a name="supported-web-browsers"></a>Desteklenen web tarayıcıları

Kullanıcılar, belirtilen işletim sistemlerinde çalışan aşağıdaki web tarayıcılarından herhangi birini kullanarak Microsoft Dynamics 365 Human Resources uygulamasına erişebilir: 

*   Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)
*   Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
*   Google Chrome (genel yayımlanmış en son sürüm)
*   Apple Safari (genel yayımlanmış son sürüm)

Her web tarayıcısı için en son sürümü bulmak için, yazılım üreticisinin web sitesine gidin. 

## <a name="special-considerations"></a>Özel hususlar

* Görev Kaydedici'nin ekran görüntüleri yakalamasını ve bunları oluşturulan Microsoft Word belgelerine dahil etmesini sağlamak için Chrome uzantısının bir ön sürümünü yüklemeniz gerekir
* İş Akışı Düzenleyicisi bir ClickOnce uygulaması olarak başlatılır. Yalnızca Microsoft Edge ve Internet Explorer (desteklenen bir Microsoft Windows sürümü üzerinde) ClickOnce uygulamalarını destekler. İş Akışı Düzenleyicisi ClickOnce uygulaması için 64-bit uyumlu bir işletim sistemi gereklidir.
* PDF dosyalarının önizlemesini yapmak için (en son sürüm genel kullanıma açık) Windows 10 üzerinde, Microsoft Edge veya (en son sürüm genel kullanıma açık) Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome gibi modern tarayıcıları kullanmanızı öneririz.

## <a name="network-requirements"></a>Ağ gereksinimleri

* İnsan Kaynakları 250-300 milisaniye (ms) veya daha az gecikmeye sahip ağlar için tasarlanmıştır. Bu, bir tarayıcı istemcisinden İnsan Kaynakları'nı barındıran Microsoft Azure veri merkezine iletim süresidir. Ağ gecikmesini [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test") adresinde sınamanızı öneririz.
* İnsan Kaynakları için bant genişliği gereksinimlerini senaryoya bağlıdır. Tipik senaryolar 50 kilobayt/saniye (KB/sn) üzerinde bir bant genişliği gerektirir.
 
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
