---
title: Süreklilik programı kullanma
description: Bu yordam, süreklilik programının satılmasını ve ilgili satış siparişlerinin işlenmesini gösterir.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
ms.openlocfilehash: 3736984a336b35b23b7060b2d98770912cc9ec6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267417"
---
# <a name="using-continuity-program"></a>Süreklilik programı kullanma

[!include [banner](../includes/banner.md)]

Bu yordam, süreklilik programının satılmasını ve ilgili satış siparişlerinin işlenmesini gösterir. Bu yordamı tamamlamak için kullanıcının bir çağrı merkezi kullanıcısı olarak ayarlanması gerekir. Bu yordam, USRT demo veri şirketini kullanır.

1. Perakende ve Ticaret > Müşterileri > Müşteri hizmetlerine gidin.
2. SearchText alanına 'Karen' yazın ve ardından Sekme tuşuna basın.
    * Gelişmiş arama iletişim kutusu açılmalıdır. Açılmazsa bu alanının sağındaki Ara'ya tıklayın.  
3. Listede, seçili satırı işaretleyin.
    * Karen Berg'i gösteren yalnızca bir satır bulunmalıdır. Tablonun en solunda yer alan onay işareti sütununa tıklayarak satırı seçin.  
4. Seç'e tıklayın.
5. Yeni satış siparişine tıklayın.
    * Satış siparişi numarasını not etmek iyi bir fikirdir. Bu yordamda daha sonra gerekir.  
6. Madde numarası alanına "88000" yazın ve ardından Sekme tuşuna basın.
    * Bu, USRT demo verilerinde bir süreklilik öğesidir.  
7. Tamamla öğesine tıklayın.
8. Ödeme yöntemi alanına "Visa" yazın.
9. Kredi kartı ekle'ye tıklayın.
    * Gerekli kredi kartı bilgilerini bu sayfada girin.  
10. Tamam'a tıklayın.
11. Ödeme bölümünü genişletin.
    * Çağrı merkezi siparişi göndermek için sipariş için ödemelerin girilmesi gerekir.  
12. Tamam'a tıklayın.
13. Gönder'i tıklatın.
    * Yeni bir süreklilik siparişi oluşturmaya hazırsınız. Ardından, süreklilik siparişlerini işlemek için kullanılan iki toplu işlemi çalıştırın.  
14. Sayfayı kapatın.
15. Perakende ve Ticaret > Süreklilik > Süreklilik ödemelerini işle'ye gidin.
16. Süreklilik maddesi alanına "88000" yazın ve ardından Sekme tuşuna basın.
17. Tamam'a tıklayın.
18. Perakende ve Ticaret > Süreklilik > Süreklilik alt siparişleri oluştur'a gidin.
    * Bu işlem, süreklilik programlarınızın ayarlarına dayanarak yeni satış siparişleri oluşturur.  
19. Süreklilik maddesi alanına "88000" yazın ve ardından Sekme tuşuna basın.
    * Madde "88000", USRT demo verilerinde bir süreklilik öğesidir.  
20. Satış siparişi alanına bir değer girin veya seçin.
    * Bu yordamda daha önce not ettiğiniz satış siparişi numarasını girin. Bu, bu yordam için işlem süresini minimumda tutar. Satış siparişi alanı isteğe bağlıdır: Tek bir programda tüm siparişleri işleyebilirsiniz.  
21. Tamam'a tıklayın.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
