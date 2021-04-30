---
title: Kira içe aktarma çerçevesi üzerinden kiraları yönetme
description: Bu konu, aynı anda birden fazla kiralamayı düzeltmek için kiralama içe aktarma çerçevesinin nasıl kullanılacağını açıklar.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseImportHeader
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 083adf0a4bb74ac65e6f8b5077f65c74eb3fa337
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880922"
---
# <a name="manage-leases-through-the-lease-import-framework"></a>Kira içe aktarma çerçevesi üzerinden kiraları yönetme

[!include [banner](../includes/banner.md)]

Bu konu, tek adımda birden fazla kiralamayı düzeltmek için kiralama içe aktarma çerçevesinin nasıl kullanılacağını açıklar. Bu özelliği kullanarak zamandan tasarruf edebilir ve insan hatası olasılığını azaltarak daha doğru düzeltmeler yapabilirsiniz. Ek olarak, bu özellik Microsoft Dynamics 365 Finance'i dış veri varlıklarıyla bağlayarak verilerin etkili şekilde karşıya yüklenmesini sağlayabilir.

Aşağıdaki veri varlıkları dış sistemlerle Varlık kiralamayı tümleştirmek için kullanılabilir:

- Kiralama hazırlığı
- Ödeme sözleşmesi hazırlığı
- Yürütme sözleşmesi hazırlığı

Bir kiralamayı düzeltmek, mali olmayan bilgileri güncelleştirmek ve yeni kiralamalar eklemek için içeri aktarma işlemini kullanabilirsiniz. Kiralama verilerini içe aktarmadan önce görüntüleyebilir ve düzenleyebilirsiniz.

Sistem, kira içe aktarma paketi aracılığıyla aşağıdaki üç işlemi çalıştırabilir.

| İşlem türü  | Tanım |
|---------------|-------------|
| Kayıt ekleme    | Bu işlem türüne sahip olan geçirilmiş kiralamalar sistemde kira oluşturur. Ödeme planı el ile onaylanmalı ve ilk kabul günlük girişi geçiş sonrasında el ile deftere nakledilmelidir. |
| Kaydı güncelleştir | Bu işlem türüne sahip olan geçirilmiş kiralamalar, zaten sistemde bulunan bir kiralama için alan değerlerini güncelleştirir. Yalnızca **Alanları güncelleştir seçimi** sayfasında seçilen alanlar güncelleştirilir. Bu işlem türü kiralamayı düzeltmediğinden, **Alanları güncelleştir seçimi** sayfasında mali olmayan alanları seçmeniz önerilir. |
| Kaydı düzelt | Bu işlem türüne sahip olan geçirilmiş kiralamalar kiralamayı düzeltir. Bu düzeltme, kiralamada mali kiralama değişikliğine neden olur. Kiralama işlendikten sonra sistem, kira içe aktarma paketindeki yeni verileri kullanarak yeni bir ödeme planı oluşturur. Sistem ödeme planını onaylamıyor veya düzeltme günlüğü girişini deftere nakletmiyor. |

**Veri yönetimi** çalışma alanı üzerinden bilgi karşıya yüklendikten sonra, **Üst bilgiyi içeri aktar** sayfasını açın (**Varlık kiralama \> Kiralama içeri aktarma çerçevesi \> Üst bilgiyi içeri aktar**). Bu sayfa, daha önce listelenen üç veri varlığının tüm içe aktarımlarını listeler.

İşlem çalıştırılmadan önce kiralama hazırlama verilerini görüntülemek için **Hazırlama verileri**'ni seçin.

Karşılaştırma işlevi, içeri aktarmakta olduğunuz bir kaydı sisteminizde zaten olan ilgili kayıtla karşılaştırmanızı sağlar. Tek bir kiralama kaydını karşılaştırmak için, bir kiralama seçin ve **Karşılaştır** ı seçin. Kiralama kayıtlarını geçirmeden önce bir **Farklar** raporu oluşturmak için bu adımı tamamlamalısınız. Karşılaştırma işlevi, hazırlama verileri içindeki değerleri, o anda sistemde bulunan kiralamaların değerleriyle karşılaştırır.

> [!NOTE]
> Karşılaştırma işlevi, **Kayıt ekleme** işlem türüne sahip kiralamalarla karşılaştırılacak bir öğe olmadığından bunlar için çalışmaz.
>
> Aynı anda birden fazla kiralamayı karşılaştırmak için **Varlık kiralama \> Kiralama içeri aktarma çerçevesi \> Periyodik** bölümüne gidin ve **Karşılaştır**'ı seçin.

Her bir varlık için, şu anda sistemdekiler ve hazırlama tablolarındakiler arasındaki farkları görüntüleyebilirsiniz. Hazırlama tablolarındaki her bir varlık için **Farklılıkları göster**'i seçin. Açılan iletişim kutusunda geçerli değer ve önerilen hazırlama değeri gösterilir.

**Yeni Değer** sütununda değiştirerek ve ardından **Hazırlamayı güncelleştir**'i seçerek hazırlama değerini de değiştirebilirsiniz.

Tüm kayıtların hata vermeden sisteme getirilmesini sağlamak için kiralamaları doğrulayabilirsiniz. Kiralama kaydı geçirilmeden önce, sistem kaydın başarıyla içeri aktarıldığından emin olmak için birkaç doğrulama çalıştırır. Tek bir kirayı doğrulamak için **Doğrula**'yı seçin.

> [!NOTE]
> Aynı anda birden fazla kiralamayı doğrulamak için **Varlık kiralama \> Kiralama içeri aktarma çerçevesi \> Periyodik** ve **Doğrula**'yı seçin.

Tek bir kirayı işlemek için **Üst bilgiyi içeri aktar** sayfasında **Kiralama kayıtlarını geçir**'i seçin. Bir kiralama geçirildiğinde sistem, **İşlem türü** alanında belirtilen işlemi gerçekleştirir.

> [!NOTE]
> Aynı anda birden fazla kiralamayı taşımak için **Varlık kiralama \> Kiralama içeri aktarma çerçevesi \> Periyodik** bölümüne gidin ve **Geçir**'i seçin.

Kiralamalar karşılaştırıldıktan sonra, içeri aktarma kimliğine dahil edilen her kiralama için farkları görüntülemek amacıyla bir rapor çalıştırabilirsiniz. Raporu bir kiralama için çalıştırmak istiyorsanız hazırlama verilerinde bu kiralamayı seçin ve ardından **Karşılaştır ve raporu görüntüle \> Farklar raporu** öğesini seçin.

> [!NOTE]
> Aynı anda birden fazla kiralamayı karşılaştırmak için **Varlık kiralama \> Kiralama içeri aktarma çerçevesi \> Periyodik** bölümüne gidin ve **Karşılaştır**'ı seçin. 

## <a name="set-up-update-fields"></a>Güncelleştirme alanlarını ayarlama

Kiralama içeri aktarma çerçevesini, kiraları güncelleştirmek için kullanıyorsanız ve işlem türü **Kaydı güncelleştir** ise, güncelleştirilecek belirli alanları seçebilirsiniz.

1. **Varlık Kiralama \> Kiralama içeri aktarma çerçevesi \> Kurulum \> Alanı güncelleştir seçimi** bölümüne gidin.
2. Görüntülenen sayfada güncelleştirilecek alanları seçin ve sonra bunları **Seçili alanlar** listesine taşımak için yeşil oku seçin. Yalnızca **Seçili alanlar** listesindeki alanlar kira içeri aktarma paketi kullanılarak güncelleştirilebilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
