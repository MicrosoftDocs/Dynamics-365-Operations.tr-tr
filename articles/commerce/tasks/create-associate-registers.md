---
title: " Kayıtlar oluşturma ve ilişkilendirme"
description: Bu yordam, bir satış noktası (POS) kaydının nasıl oluşturulacağını gösterir.
author: rubencdelgado
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba978a3d895394760687386197dbb3512c62ef98
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798573"
---
# <a name="create-and-associate-registers"></a> Kayıtlar oluşturma ve ilişkilendirme

[!include [banner](../includes/banner.md)]

Bu yordam, bir satış noktası (POS) kaydının nasıl oluşturulacağını gösterir. Bu yordam, USRT demo verisi şirketini kullanır.

1. Retail and Commerce > Kanal kurulumu > POS kurulumu > Kayıtlar'a gidin.
2. Yeni'yi tıklatın.
3. Kayıt numarası alanında yeni kayıt için bir Kimlik yazın.
    * Kayıt kodu, genel olarak kaydın ait olduğu mağaza ve mağaza içindeki konum ile eşleşmesine yardımcı olan kodlar içerir.  
4. Ad alanına kayıt için açıklayıcı bir ad yazın.
5. Mağaza numarası alanına bir değer girin veya bir değer seçin.
6. Donanım profili alanına bir değer girin veya bir değer seçin.
    * Donanım profilleri, yazar kasa çekmecesi ve fatura yazıcısı gibi kayıt cihazına bağlanacak aksesuarlarını belirlemek için kullanılır.  
7. Görsel profil alanına bir değer girin veya bir değer seçin.
    * Sanal profiller, POS arka planında ve oturum açma sayfasında kullanılan görüntüleri belirlemek ve POS temaları için kullanılır.  
8. EFT POS kayıt numarası alanına bir değer girin.
    * EFT POS kayıt numarası, ödeme terminalinin yetkilendirme talepleri gönderdiği ödeme işlemcisini bilgilendirmek için kullanılır. Bu değere genellikle "Terminal Kodu" veya “TID” adı verilir. TID'yi genel olarak ödeme cihazının üzerinde bir etiket üzerinde bulabilirsiniz.  
9. Kaydet'e tıklayın.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]