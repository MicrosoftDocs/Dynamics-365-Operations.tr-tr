---
title: Teminat mektupları
description: Bu makalede, teminat mektupları hakkında bilgiler verilmektedir. Teminat mektubunda bir banka, müşterilerinin bir kişiye ödeme veya yükümlülüğünü varsayılan olarak belirlediği zaman, o banka o kişiye belirli tutarda bir parayı ödemeyi kabul eder.
author: angelad116
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: kfend
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a36ab23e15d99bcaec84beb56d0ae8e33ebe6b8d
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151296"
---
# <a name="letters-of-guarantee"></a>Teminat mektupları

[!include [banner](../includes/banner.md)]

Bu makalede, teminat mektupları hakkında bilgiler verilmektedir. Teminat mektubunda bir banka, müşterilerinin bir kişiye ödeme veya yükümlülüğünü varsayılan olarak belirlediği zaman, o banka o kişiye belirli tutarda bir parayı ödemeyi kabul eder. 

Garanti mektubu, bir banka (garantör) tarafından verilen bir anlaşmadır ve banka bu anlaşmayla banka müşterisinin (muhatap) bir kişiye (lehtar) ödemesini yapmaması veya bu kişiye karşı bir yükümlülüğünü yerine getirmemesi durumunda bu kişiye belirlenen miktarda parayı ödemeyi garanti eder. Garanti mektupları transfer edilemez. Sadece anlaşmada adı geçen lehtar için geçerlidir. Muhatap, anlaşma hükümlerine bağlı olarak, garanti mektubunun değerinde artış veya azaltma talep edebilir. 

Bir garanti mektubunun likiditeye çevrilebilmesi için lehtarın mutlaka garanti belgesinin orijinalini sunması ve geçerlilik bitiş tarihinden önce muhatabın borcunu ödemediğini bankaya bildirmesi gerekir. Banka daha sonra garanti mektubunun hükümlerine dayalı olarak, lehtarın hesabına borç tutarını öder. Banka, kar olarak ödemeden bir yüzde ayırır. Bu yüzde, taraflar arasında anlaşma yoluyla belirlenir ve anlaşma hükümlerine yazılır. 

Garanti mektubunun amacını izlemek için bir kod oluşturabilirsiniz. Ayrıca, bir garanti mektubu iptal edildiğinde mektupla ilişkilendirilebilecek nedenleri belirletebilirsiniz. Amaç kodlarını ve banka nedenlerini **Ödeme amacı kodları** ve **Banka nedenleri** sayfalarında görebilirsiniz. 

**Garanti mektubu** sayfasını şu görevleri tamamlamak için kullanabilirsiniz:

-   Doğru defter girişleri oluşturma ve el ile girişi ortadan kaldırma.
-   Tüm parasal ve parasal olmayan hareketleri kaydetme ve garanti mektuplarının bakiyelerini takip etme.
-   Garanti mektuplarının durumlarını ve geçerlilik bitiş tarihlerini kaydetme ve takip etme.
-   Elinde garanti mektubu bulunan bankları listeleyen bir rapor oluşturma.

Aşağıdaki tabloda garanti mektubunda gerçekleştirebileceğiniz eylemler açıklanmıştır.

| Eylem              | Amaç                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| Bankaya gönderilen      | Bankaya garanti mektubu talebi gönderin.                                                                       |
| Bankadan alınan   | Banka, gönderilen talebi kabul ettiğinde bankadan garanti mektubunu teslim alın.                            |
| Lehdara verilen | Garanti mektubunu bankadan teslim aldığınızda garanti mektubunu muhataba verin.              |
| Değer artışı      | Lehtar ve muhatap anlaşmaya varırsa parasal değerini yükseltin.                                                  |
| Değer azalışı      | Lehtar ve muhatap anlaşmaya varırsa parasal değerini düşürün.                                                  |
| Uzat              | Garanti mektubunu lehtara verdikten sonra, uzatma gerekiyorsa geçerlilik süresini uzatın. |
| İptal              | Garanti mektubunun talep edildiği amaç artık geçerli değilse, anlaşmayı iptal edin.                  |
| Tasfiye et           | Lehtar, garanti mektubunu bankaya sunduğunda garanti mektubunu paraya çevirin.                      |


Daha fazla bilgi için aşağıdaki konulara bakın:

[Teminat mektubu hareketi](tasks/letter-guarantee-transaction.md)

[Teminat mektupları için banka hizmetlerini ve banka deftere nakil profillerini ayarlama](tasks/set-up-bank-facilities-posting-profiles.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
