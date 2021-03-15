---
title: Satış vergisi atama ve geçersiz kılma
description: Bu yordam ticaret kanallarına satış vergisi gruplarının nasıl atanacağını gösterir.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c6e1de5046a3ce5d896ba3686a28d6d474d4268
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020741"
---
# <a name="sales-tax-assignment-and-overrides"></a> Satış vergisi atama ve geçersiz kılma

[!include [banner](../../includes/banner.md)]

Bu yordam ticaret kanallarına satış vergisi gruplarının nasıl atanacağını gösterir. Ayrıca, yeni bir satış vergisi geçersiz kılma işlemi oluşturma ve mevcut bir satış vergisi geçersiz kılma grubuna atama işleminin üzerinden geçer. Bu yordam USRT demo veri şirketini kullanır.

1. Perakende ve Ticaret > Kanallar > Mağazalar > Tüm mağazalar'a gidin.
2. Listede, "Houston" için Kanalı Kodu bağlantısına tıklayın.
3. Düzenle'ye tıklayın.
    * "Satış vergisi grubu" alanı mevcut şirket için satış vergisi gruplarının listesini içerir. Mevcut atanan grup, genel bir "Teksas" satış vergisi grubudur. "Washington" ve "Washington, King County" için satış vergi grupları vardır. Satış vergisi grupları birden fazla belediye için vergileri içerebilir.  
    * "Satış vergisi geçersiz kılma" alanı satış vergisi geçersiz kılma gruplarının kanala eşlenebildiği yerdir. Satış vergisi geçersiz kılma grupları birden fazla mağaza için çalışan satış vergisi geçersiz kılma işlemlerini gruplamak için kullanılabilir. Satış vergisi geçersiz kılma işlemlerini, el ile tek tek atamak yerine zaman kazanmak için grup oluşturulup doğrudan kanallara atanabilir.  
4. Kaydet'i tıklatın.
5. Sayfayı kapatın.
6. Perakende ve ticaret > Kanal kurulumu > Satış vergileri > Satış vergisi geçersiz kılma işlemlerine gidin.
7. Yeni'ye tıklayın.
8. Satış vergisi geçersiz kılma alanında yeni geçersiz kılma işleminize bir ad verin.
9. Açıklama alanında geçersiz kılma işleminin bir açıklamasını girin.
10. Durumu "Etkinleştir" olarak ayarlayın.
11. Geçersiz Kıl bölümünü genişletin veya daraltın.
12. Tür alanında, bir seçenek seçin.
    * Madde satış vergisi grubu, gruba ait olan belirli maddeler için vergileri geçersiz kılmak için kullanılabilir. Örneğin, yiyecek maddeleri genellikle bozulmaz mallardan farklı olarak vergilendirilir ve büyük ihtimalle kendilerine ait satış vergisi grubu vardır. Satış vergisi grupları, belirli bir kanala uygulanabilir vergilerin gruplarıdır. Örneğin, bir kanal hem perakende hem de işletmeler arası satış yapıyorsa, farklı maddelerin satış vergisi grupları kullanılabilir. Uygulanabilir tüm vergiler satış vergisi grubuna eşlenebilir.  
    * Şimdi satış vergisi geçersiz kılma işleminizi oluşturmak için "Kimden" ve "Kime" vergilerini veya "İlk vergi grubu" ve "Son vergi grubu" öğesini seçebilirsiniz. "Kimden" alanı, geçersiz kılınacak vergi veya vergi grubunu belirtir. Madde satış vergisi grubunu geçersiz kılma işlemi, satış vergisi grubuna göre geçersiz kılma işleminden farklı seçenekler sunar. Satış vergisi geçersiz kılma işlemleri, vergileri tüm işlemler veya işlemde belirli satırlar üzerinde geçersiz kılacak şekilde ayarlanabilir.  
13. Kaydet'i tıklatın.
14. Sayfayı kapatın.
15. Perakende ve ticaret > Kanal kurulumu > Satış vergileri > Satış vergisi geçersiz kılma grupları'na gidin.
    * Bu adımda, Houston kanalına atanmış satış vergisi geçersiz kılma grubuna yeni oluşturulan satış vergisi geçersiz kılma işlemi atayın.  
16. Düzenle öğesine tıklayın.
17. Kurulum bölümünü genişletin veya daraltın.
18. Ekle öğesini tıklatın.
19. Satış vergisi geçersiz kılma alanında, aramayı açmak için açılır düğmeye tıklayın.
20. Listeden, önceden oluşturulan satış vergisi geçersiz kılma işlemini seçin.
21. Listede, seçili satırdaki bağlantıya tıklayın.
22. Kaydet'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]