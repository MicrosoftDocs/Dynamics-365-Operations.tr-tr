---
title: Konsolidasyon için içe aktarma biçimi
description: Bu konu, birden çok tüzel kişilikten gelen finansal verileri konsolide ettiğiniz kullanılan içe aktarma biçimi hakkında ayrıntılı bilgi sağlar.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 6d25ebfedfe748dfa262c1d4b0671539e6150a0f9f05dfca42e87f23486fbb19
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746428"
---
# <a name="import-format-for-consolidation"></a>Konsolidasyon için içe aktarma biçimi

[!include [banner](../includes/banner.md)]

Bu konu, birden çok tüzel kişilikten gelen finansal verileri konsolide ettiğiniz kullanılan içe aktarma biçimi hakkında ayrıntılı bilgi sağlar. İçe aktarma biçimi, metin (.txt) dosyası olarak kaydedilmelidir.

## <a name="import-format"></a>İçe aktarma biçimi

Aşağıdaki tabloda, içeri aktarma sırasında konsolidasyon yaparken kullanmanız gereken içeri aktarma biçimi listelenmektedir.

| Kayıt tablosu | Biçim | Notlar |
|--------------|---------|-------|
| 1            | 170150, Goodwill, 4 | <ul><li>Kayıt tablosu</li><li>Kaynak ana hesap kimliği</li><li>Ana hesap satırı</li><li>Ana hesap türü</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Ana hesap kimliği</li><li>Hareket tarihi</li><li>Mali dönem türü (**0** = Açılış, **1** = Faaliyet ve **2** = Kapanış)</li><li>Hareketin para birimi</li><li>Borç veya alacak (**0** = Borç ve **1** = Alacak)</li><li>Deftere nakil katmanı</li><li>Hareket tutarları</li><li>Miktar</li><li>Yerel RecID (hareket için belirsiz, benzersiz int64 değeri)</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>Giriş numarası (bütçe başlığı hareket numarası)</li><li>Bütçe başlığının varsayılan tarihi</li><li>Bütçe modeli kimliği</li><li>Bütçe türü (**1** - Orijinal Bütçe, **2** - Transfer, **3** - Revizyon, **4** - Yükümlülük, **5** - Yükümlülük öncesi, **6** - Nakli yekun bütçesi, **7** - Proje, **8** - Sabit Kıymetliler, **9** - Talep tahmini, **10** - Arz tahmini, **11** - Paylaştırmalar, **12** - Geçici bütçe.)</li><li>Satırın tarihi</li><li>Satır için ana hesap</li><li>Satır için para birimi kodu</li><li>Hareket para birimi cinsinden satırın tutarı</li><li>Satırın bütçe türü için sabit listesi tamsayı değeri (gider veya gelir)</li></ul> |
| 4            | DEMF | RecordCompany, Kaynak tüzel kişiliktir. |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Ana hesap kodu</li><li>Hareket tarihi</li><li>Mali dönem türü (0 Açılış, 1 Faaliyet ve 2 Kapanış)</li><li>Hareket para birimi</li><li>Borç veya alacak (0 Borç ve 1 Alacak)</li><li>Deftere nakil katmanı</li><li>Hareket tutarı</li><li>Miktar</li><li>Yerel RecID (hareket için belirsiz, benzersiz int64 değeri)</li></ul>  |
| 6            | İş Kolu, 1 Departman, 2 | Segment emrinde tanımlanan mali boyut öznitelikleri.<p>Özniteliklerin nasıl tanımlandığını doğrulamak için **Dışarı Aktar** sayfasını kullanabilirsiniz.</p> |
| 7            | 002,1,658 | <ul><li>Mali boyut değeri</li><li>RecordDimensions'da sağlanan dizin olarak mali boyut</li><li>RecordTrans veya RecordTrans2'deki benzersiz kayıt kimliğiyle ilişkili belirsiz, benzersiz kayıt kimliği</li></ul> |
| 8            | 002,1,1 | <ul><li>RecordBudget'taki hareketle ilişkili boyut değerleri</li><li>RecordDimensions'da sağlanan dizin olarak mali boyut</li><li>Dosyadaki hareket satırlarının sırasına göre hizalanmış belirsiz bir satır kaydı kimliği</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
