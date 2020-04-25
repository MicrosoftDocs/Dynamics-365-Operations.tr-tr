---
title: İade edilen maddelerin girişini kaydetme
description: İade edilen maddelerin girişini Varış özeti formunu veya Kayıt formunu kullanarak kaydedebilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9979c6180bda406513cc3234c9fa5d9db2b32a75
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202089"
---
# <a name="register-the-receipt-of-returned-items"></a>İade edilen maddelerin girişini kaydetme 

[!include [banner](../includes/banner.md)]


İade edilen maddelerin girişini kaydetmek için iki yöntem bulunur. İlk yöntem **Varış özeti** formunu kullanan ambar alma sürecidir. İkinci yöntem **Kayıt** formunu kullanır.

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a>İade edilen maddelerin girişini Varış özeti formuna kaydetme

**Varış özeti** formunu bir iade sevkiyatını İade Malzemeler İzni (RMA) numarasına göre tanımlamak için kullanabilirsiniz. **Kurulum** sekmesinde bir günlük adı tanımlandıysa ve **Varış özeti** formunda seçili satırlara karşılık gelen günlük satırları varsa **Varışı başlat**'a tıkladığınızda yeni bir günlük başlığı oluşturulur.

1.  **Stok yönetimi** \> **Periyodik** \> **Varışa genel bakış**'a tıklayın.

2.  **Kurulum adı** alanında, **İade siparişi**'ni seçin ve ardından **Güncelleştir**'e tıklayın.
    

    > [!TIP]
    > <P>Arama sonuçlarını daraltmak için <STRONG>Aralık</STRONG> alanlarını kullanabilirsiniz. Kesin bir sonuç için <STRONG>RMA numarası</STRONG> alanına RMA numarasını yazabilirsiniz. Hangi gelen varışların görüntüleneceğini sınırlandıran filtre kümesini tanımlamak ve kaydetmek için <STRONG>Kurulum</STRONG> sekmesine tıklayın. Kullanılabilir filtreler türleri, ambarları ve noktaları içerir.</P>

    

    > [!WARNING]
    > <P>İade siparişleri <STRONG>Varış özeti</STRONG> formundaki diğer varış türleriyle karıştırılamaz. Bu nedenle, referans daima satış siparişi olacaktır ancak günlük başlığında satış siparişi kodu belirtilmeyecektir.</P>



3.  **Girişler** ızgarasında iade edilen maddeyle eşleşen satırı bulun ve sonra **Varış için seç** sütununda onay kutusunu seçin.

4.  Örneğin orijinal siparişten iade sevkiyatına dahil edilmeyen maddeler gibi belirli satırları iade girişinin dışında tutmak için formun alt bölümündeki **Satırlar** tablosunda bulunan ilgili **Varış için seç** onay kutularını temizleyin.

5.  Bir varış günlüğü oluşturmak için **Varışı başlat** düğmesine tıklayın.
    

    > [!NOTE]
    > <P>Birden fazla iade siparişi seçebilir ve tümünü tek bir varış işlemine dahil edebilirsiniz. Her iade siparişi satırı karşılık gelen varış günlüğü satırına kopyalanır.</P>

    

    > [!NOTE]
    > <P><STRONG>Madde varışı</STRONG> formunu kullanarak bir varış günlüğünü el ile de oluşturabilirsiniz. 



6.  **Stok Yönetimi** \> **Günlükler** \> **Madde varışı** \> **Madde varışı**'na gidin.

7.  Yeni oluşturduğunuz varış günlüğünü seçin ve **Satırlar**'ı tıklayarak **Günlük satırları, yerleşimler** formunu açın.

8.  **Genel** sekmesinde **Miktar** alanında sayıyı düzeltin ve gerekirse **Elden çıkarma kodu** alanında bir elden çıkarma kodu atayın.
    
    Alternatif olarak, İade edilen maddelerin bir karantina emri bağlamında denetleme işlemine gönderilmesini sağlamak için **Karantina yönetimi** onay kutusunu seçebilirsiniz.
    

    > [!NOTE]
    > <P>İade edilen maddeleri karantina yoluyla gönderirseniz, bir elden çıkarma kodu belirtemezsiniz.</P>



9.  **Doğrula** düğmesine tıklayın.

10. Doğrulama sürecinde hata yoksa **Deftere naklet** seçeneğine tıklayın.

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a>İade edilen maddelerin girişini Kayıt formuna kaydetme

**Varış özeti** formunu kullanmaya alternatif olarak iade edilen maddelerin varışını kaydetmek için **Kayıt** formunu kullanabilirsiniz.

1.  **Satış ve pazarlama** \> **Genel** \> **İade siparişleri** \> **Tüm iade siparişleri**'ne tıklayın. Yeni bir iade siparişi oluşturun veya iade siparişini listeden açın. **Satırlar** hızlı sekmesinde iade siparişi satırını seçin. **Satırı güncelleştir**'e ve ardından **Kayıt**'a tıklayın.

2.  **Elden çıkarma kodu** alanında bir elden çıkarma kodu atayın ve **Tamam**'a tıklayın.
    

    > [!NOTE]
    > <P><STRONG>Kayıt</STRONG> formu kullanıldığında maddeyi bir karantina emri olarak denetime göndermek mümkün değildir.</P>



3.  **Hareketler** ızgarasında, kaydedilecek hareketi seçin.

4.  **Şimdi kaydet** ızgarasında **Ekle**'ye tıklayın. Tüm iade edilen maddeler **Şimdi kaydet** ızgarasında görünene kadar önceki iki adımı tekrarlayın.

5.  **Tümünü deftere naklet**'e tıklayın.

## <a name="see-also"></a>Ayrıca bkz.

[Varış özeti (form)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))

  


