---
title: Çapraz kuru belirtme
description: Bu konuda, Microsoft Dynamics 365 Finance'teki çapraz kurlar hakkında bilgi verilmektedir.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 146794557a3a6ba1801598fe6b814e209d9f5fc6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448657"
---
# <a name="specify-the-cross-rate"></a>Çapraz kuru belirtme

[!include [banner](../includes/banner.md)]

Bu konu, çapraz kurun amacını ve faturaya karşılık bir ödemeyi kapattığınız zaman çapraz kurun nasıl belirtileceğini açıklar. Aşağıdaki ölçütlerin tümü geçerliyse bir çapraz kur kullanın: 
-   Faturaya karşılık bir ödemeyi kapatıyorsunuz. 
-   Ödeme satırı ve fatura satırı farklı para birimleri kullanıyor. 
-   Para birimlerinin her ikisi de muhasebe para birimi değil. 

Çapraz kur, ödeme hareketi para birimini ödeme muhasebe para birimine dönüştürmeyi hesaplamak için kullanılmaz. Bunun yerine, ödeme hareketinin para birimi tutarı ve ödeme muhasebe para birimi tutarı değerini hesaplamak için döviz kurları tablolarından döviz kurları alınır. 

Örneğin, muhasebe para birimi USD, fatura para birimi CAD ve ödeme para birimi EUR olsun. Çapraz kur, CAD ve EUR arasında doğrudan (USD üzerinden dönüştürmeye gerek kalmadan) dönüştürmek için bir döviz kuru girmenize olanak sağlar. Bir fatura ve bir birincil ödeme seçerken fatura satırı için bir çapraz kur girebilirsiniz. Çapraz kur, kapatma tarihi itibariyle bu hareketlerin para birimleri arasındaki döviz kurudur.

1.  Aşağıdaki sayfalardan birine gidin:
- **Alacak hesapları > Genel > Müşteriler > Tüm müşteriler** 
- **Borç hesapları > Genel > Satıcılar > Tüm satıcılar** 
- **Tedarik ve kaynak atama > Genel > Satıcılar > Tüm satıcılar**
2.  Açık hareketlerini kapattığınız müşteri veya satıcıyı seçin. 
3.  Müşteri için, **Tüm müşteriler** liste sayfasında **Tahsil et > Açık hareketleri kapat**'a gidin. Satıcı için, **Tüm satıcılar** liste sayfasında **Fatura > Açık hareketleri kapat**'a gidin. 
4.  Birincil ödeme olan hareketi seçin ve **Ödemeyi işaretle**'ye tıklayın. **İşaret** sütunundaki onay kutusu işaretlenir ve **Birincil ödeme** sütununda bir bilgi simgesi görünür. 
5.  **Çapraz kur** alanına, fatura para birimi ve ödeme para birimi arasında kapatma tarihi itibariyle geçerli olan döviz kurunu girin. 
