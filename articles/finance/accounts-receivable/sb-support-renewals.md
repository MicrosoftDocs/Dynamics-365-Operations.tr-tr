---
title: Destek ve yenilemeler
description: Bu konu, yenileme maddeleri için bir faturalama planı oluşturmak üzere satış siparişlerinde destek ve yenileme işleminin nasıl ayarlanacağını ve kullanılacağını açıklamaktadır.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d59eee6e858c4f0051ec103adc4e1e99e79feec9
ms.sourcegitcommit: 4d7bc52e6cdf6afce3793893ba2aa07176302314
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/11/2022
ms.locfileid: "8560499"
---
# <a name="support-and-renewals"></a>Destek ve yenilemeler 

Bu konu, satış siparişleri girdiğinizde destek maddelerinin veya yenileme maddelerinin nasıl kullanılacağını açıklar. Bu maddeler, orijinal destek sözleşmesinin gider tutarını hesaplamak ve/veya abonelik faturalaması sırasında bir faturalama planı oluşturulduğunda kullanılan yenileme tutarını hesaplamak için kullanılır. Örneğin, şirketiniz müşteriye bir sunucu satıyor ve ilk yıl için bir veri yedekleme aboneliği ve bu aboneliği her yıl yenileme seçeneği sağlıyor. *Destek maddesi*, ilk yılın aboneliğidir ve *yenileme maddesi*, bunu izleyen her yıl için yenilemedir.

Destek sözleşmesi, yenileme sözleşmesi veya her ikisi için bilgi girebilirsiniz. Destek sözleşmesi bilgilerini girdiğinizde, satış siparişine yalnızca destek maddesi eklenir. Yenileme sözleşmesi bilgilerini girdiğinizde, yenileme maddesi bir faturalama planı oluşturmak için kullanılır.

## <a name="support-and-renewal-setup"></a>Destek ve yenileme kurulumu

**Destek ve yenileme düzeyleri** sayfasında, destek ve yenileme maddeleri için farklı destek düzeyleri ayarlayabilirsiniz. Destek veya yenileme, orijinal madde miktarının yüzdesi olabilir veya standart bir tutar olabilir.

**Yinelenen sözleşme faturalama parametreleri** sayfasında varsayılan destek düzeylerini seçebilirsiniz.

Örneğin, bir şirket aşağıdaki destek ve yenileme düzeylerini sunabilir.

| Destek düzeyi | Destek yüzdesi | Yenileme yüzdesi |
|---|---|---|
| Sınırsız | %40 | %30 |
| Sarı | %25 | %18 |
| Gümüş | %20 | %14 |
| Bronz | %15 | %10 |

Destek veya yenileme düzeyi oluşturmak için aşağıdaki adımları izleyin.

1. **Destek ve yenileme düzeyleri** sayfasında, **Yeni**'yi seçin.
2. **Destek düzeyi** alanında benzersiz bir ad girin.
3. **Açıklama** alanına bir açıklama girin.
4. **Destek hesaplama yöntemi** alanında, destek hesaplama yöntemini seçin. **Yüzde**'yi seçerseniz, **Destek yüzdesi** alanına bir destek yüzdesi girin.
5. **Yenileme hesaplama yöntemi** alanında, yenileme hesaplama yöntemini seçin. **Yüzde**'yi seçerseniz, **Yenileme yüzdesi** alanına bir yenileme yüzdesi girin.
6. **Kaydet**'i seçin.

### <a name="fields"></a>Alanlar

**Destek ve yenileme düzeyleri** sayfası aşağıdaki alanları içerir.

| Alan | Açıklama |
|---|---|
| Destek düzeyi | Destek veya yenileme düzeyi için benzersiz tanımlayıcı (örneğin, **Altın** veya **Gümüş**). |
| Açıklama | Destek veya yenileme düzeyinin açıklaması. |
| Destek hesaplama yöntemi | Düzey için destek hesaplama yöntemini seçin: **Yüzde** veya **Standart tutar**. |
| Destek yüzdesi | Destek hesaplama yöntemi olarak **Yüzde**'yi seçtiyseniz, destek maddesinin fiyatını hesaplamak için kullanılacak yüzdeyi belirtin. Hesaplama yöntemi olarak **Standart tutar**'ı seçtiyseniz tutar, hareket oluşturulduğunda belirtilir. |
| Yenileme hesaplama yöntemi | Düzey için yenileme hesaplama yöntemini seçin: **Yüzde** veya **Standart tutar**. |
| Yenileme yüzdesi | Yenileme hesaplama yöntemi olarak **Yüzde**'yi seçtiyseniz, yenileme maddesinin fiyatını hesaplamak için kullanılacak yüzdeyi belirtin. Hesaplama yöntemi olarak **Standart tutar**'ı seçtiyseniz tutar, hareket oluşturulduğunda belirtilir. |

## <a name="support-and-renewal-process"></a>Destek ve yenileme işlemi

Destek ve yenileme işlevi, maddelere farklı destek düzeyleri uygulayabilir ve abonelik faturalamasında yenileme bilgilerini güncelleştirebilir.

Destek ve yenileme işlevselliğini kullanmadan önce, aşağıdaki görevlerin tamamlanması gerekiyor.

1. **Destek ve yenileme düzeyleri** sayfasında, en az bir destek veya yenileme düzeyi oluşturun.
2. **Madde kurulumu** sayfasında, bir maddeyi destek ve yenileme maddeleriyle ilişkilendirin. Bu görev yalnızca destek ve/veya yenileme maddeleri için varsayılan değerler ayarlamak istediğinizde gereklidir.
3. **Yinelenen sözleşme faturalama parametreleri** sayfasında, yeni faturalama planları için varsayılan destek ve yenileme ayarlarını belirtin.

Maddelere farklı destek düzeyleri uygulamak ve yenileme bilgilerini güncelleştirmek için aşağıdaki adımları izleyin.

1. **Tüm satış siparişleri** sayfasında bir satış siparişi oluşturun.
2. **Satış siparişleri satırları** hızlı sekmesinde bir madde ekleyin.
3. **Fatura** sekmesinde, **Destek ve yenileme \> Destek ve yenileme ekle**'yi seçin.
4. **Destek ve yenileme işlemi** sayfasında başlık bölümü, **Yinelenen sözleşme faturalama parametreleri** sayfasındaki ayarlarla güncelleştirilir. Bu değerler tüm destek ve yenileme maddelerine uygulanır. (Örneğin, faturalama sıklığı **Yıllık** olarak ayarlanmışsa, yenileme maddesi bulunan oluşturulmuş tüm satış satırlar yıllık sıklığa sahip olur.) Satış siparişini varolan bir faturalama planıyla ilişkilendirmek için, **Faturalama planı numarası** alanında bir değer seçin.
5. Destek veya yenileme başlangıç tarihini değiştirmek için, **Başlangıç tarihini geçersiz kıl** seçeneğini **Evet** olarak ayarlayın.
6. Destek maddesi eklemek veya düzenlemek için, **Destek** onay kutusunu seçin ve **Destek maddesi** alanına bir destek maddesi girin. Madde var olan satış siparişine eklenir.
7. Yenileme maddesi eklemek veya düzenlemek için, **Yenileme** onay kutusunu seçin ve **Yenileme maddesi** alanına bir yenileme maddesi girin. Satış siparişi faturalandığında, maddeyi içeren bir faturalama planı oluşturulur.
8. **Tamam**'ı seçin.
9. **Oluştur** sekmesinde, **Fatura**'yı seçin. Satış siparişi deftere nakledildiğinde, faturalama planı oluşturulur. Faturalama planı bilgilerini içeren bir bildirim ileti ayrıntılarında görüntülenir.
10. **Tüm/Etkin faturalama planları** listesi sayfasında **Faturalama planları** sayfasındaki faturalama planı ayrıntılarını gözden geçirmek için faturalama planı numarasını seçin.
11. **Faturalama planı satırları** hızlı sekmesinde, oluşturulan satırların ayrıntılarını gözden geçirmek için **Destek ve yenileme**'yi seçin.

> [!NOTE]
> Bir faturalama planı satırı için yenileme başlangıç tarihi değiştirilirse, **Faturalama planları** sayfasındaki satır için **Başlangıç tarihi** değerini düzenleyebilirsiniz. Satır için **Ödeme ayrıntılarını görüntüle** sayfasını açtığınızda, **Faturalama başlangıç tarihi** alanı yeni tarihle güncelleştirilir. **Faturalama bitiş tarihi** değeri, faturalama sıklığı temel alınarak yeniden hesaplanır. Yenileme başlangıç tarihi yalnızca yenileme faturalama planının ilk faturası oluşturulmamış ve deftere nakledilmemişse güncelleştirilebilir. İlk fatura oluşturulup deftere nakledildikten sonra, başlangıç tarihi düzenlenemez.

Destek ve yenileme işlemi yalnızca satış siparişi için kullanılabilir. Bir satış siparişine destek ve yenileme maddeleri eklediğinizde, yeni bir faturalama planı oluşturabilir veya varolan bir faturalama planına yenileme maddesi ekleyebilirsiniz.

## <a name="support-and-renewal-audit"></a>Destek ve yenileme denetimi

**Destek ve yenileme denetimi** sayfasında, bir satış siparişindeki yenileme maddesinden oluşturulan faturalama planı satırlarının ayrıntılarını gözden geçirebilirsiniz. Bu seçenek yalnızca, faturalama planı satır maddesi bir yenileme maddesi olduğunda kullanılabilir.

Bir faturalama planı satırı için destek ve yenileme bilgilerini düzenlemek üzere aşağıdaki adımları izleyin.

1. **Tüm faturalama planları** sayfasında faturalama planı numarasını seçin.
2. **Faturalama planı satırları** bölümünde, bir satırı ve ardından **Destek ve yenileme**'yi seçin.
3. Destek veya yenileme maddesiyle ilgili tüm bilgileri gözden geçirin.
4. Destek düzeyinde veya yenileme yüzdesi ya da tutarında gerekli tüm değişiklikleri yapın ve sonra **Değişiklik nedeni** alanına bir değer girin.
5. **İşlem**'i seçin.

### <a name="fields"></a>Alanlar

**Destek ve yenileme denetimi** sayfası aşağıdaki alanları içerir.

| Alan | Açıklama |
|-------|-------------|
| Madde numarası | Faturalama planı satırının madde numarası. |
| Ürün adı | Ürün adı. |
| Destek planı düzeyi | Yenileme maddesinin destek düzeyini görüntüleyin veya değiştirin. |
| Yenileme yüzdesi | Bir faturalama planında yenileme maddesi için birim fiyat hesaplanırken kullanılan yenileme yüzdesini girin. |
| Yenileme tutarı | Bir faturalama planında yenileme maddesi için birim fiyat hesaplanırken kullanılan yenileme tutarını girin. |
| Değişiklik nedeni | Destek ve yenileme bilgilerini değiştirme nedeninizi girin. **Yenileme yüzdesi**, **Yenileme tutarı** veya **Destek planı düzeyi** değerini değiştirdiğinizde bir neden girmeniz gerekir. |
| Orijinal satış maddesi | Satış siparişinden alınan orijinal satış maddesi numarası. |
| Orijinal net tutar | Maddenin orijinal net tutarı. |
| Orijinal destek düzeyi | Maddenin orijinal destek düzeyi. |
| Orijinal yenileme yüzdesi | Maddenin orijinal yenileme yüzdesi. |
| Orijinal yenileme tutarı | Maddenin orijinal yenileme tutarı. |
| **Kılavuz** | |
| Orijinal destek düzeyi | Önceki destek düzeyi. |
| Orijinal yenileme yüzdesi | Önceki yenileme yüzdesi. |
| Orijinal yenileme tutarı | Önceki yenileme tutarı. |
| Değiştiren | Değişikliği yapan kullanıcının kullanıcı adı. |
| Değiştirilme tarihi ve saati | Değişikliğin oluştuğu tarih. |
| Neden | Değişikliğin nedeni. |
