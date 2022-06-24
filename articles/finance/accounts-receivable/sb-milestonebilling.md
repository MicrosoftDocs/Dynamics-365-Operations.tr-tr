---
title: Kilometre taşı şablonları
description: Bu makalede Abonelik faturalamasında aşama bazında faturalama işlevini ayarlama açıklanmaktadır.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d3c2cf751e4998c73bc3816e5b81e8d5963c8e53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856784"
---
# <a name="milestone-billing"></a>Aşama bazında faturalama

[!include [banner](../includes/banner.md)]

Bu makale Abonelik faturalamasındaki aşama bazında faturalama işlevi için şablonlar tanımlama açıklanmaktadır. Kilometre taşı şablonundaki her satır için tahsisat yüzdesini veya miktarını tanımlayabilirsiniz. Ardından kilometre taşı şablonunu aşama bazında faturalama işlevini kullanan faturalama zamanlaması maddelerine atayabilirsiniz.

## <a name="add-a-template"></a>Şablon ekle

Kilometre taşı şablonu eklemek için bu adımları izleyin.

1. **Abonelik faturalaması \> Yinelenen sözleşme faturalaması \> Kurulum \> Kilometre taşı şablonları**'na gidin.
2. **Yeni**'yi seçin.
3. **Kilometre taşı şablonu** alanına, yeni şablon için benzersiz bir tanımlayıcı girin.
4. **Açıklama** alanına bir açıklama girin.
5. **Tahsisat yöntemi** alanında, bir tahsisat yöntemi seçin.
6. İsteğe bağlı: **Toplam tutar** alanında, şablon için toplam tutarı belirtin.
7. Bir satır eklemek için **Ekle**'yi seçin. Ardından **Madde numarası** alanında, yeni satır için madde numarası seçin.
8. **Tahsisat yöntemi** alanında seçtiğiniz değere bağlı olarak, aşağıdaki adımlardan birini izleyin:

    - Tahsis yöntemi olarak **Yüzde**'yi seçtiyseniz **Yüzde** alanında her satır için tahsisat yüzdesini belirtin. Yüzde belirtirseniz **Toplam yüzde** alanında gösterilen yüzdelerin toplamı **100**'e eşit olmalıdır.
    - Tahsis yöntemi olarak **Değişken tutar**'ı seçtiyseniz **Tutar** alanında her satır için tutarı belirtin.
    - Tahsisat yöntemi olarak **Eşit tutar**'ı seçtiyseniz bir tutar belirtmeniz gerekmez. Her satır şablona eklenen madde sayısına göre doğru yüzde ve tutarla güncelleştirilir.

9. **Kaydet**'i seçin.

## <a name="delete-a-template"></a>Şablonu silme

Kilometre taşı şablonu silmek için bu adımları izleyin.

1. Silinecek bir veya daha fazla satırı ve ardından **Sil**'i seçin.
2. Eylemi onaylamanız istendiğinde **Evet**'i seçin.

## <a name="milestone-template-fields"></a>Kilometre taşı şablonu alanları

**Kilometre taşı şablonu** sayfası, aşağıdaki alanları içerir.

| Alan | Açıklama |
|-------|-------------| 
| Kilometre taşı şablonu | Kilometre taşı şablonunun benzersiz tanımlayıcısı. |
| Açıklama | Kilometre taşı şablonunun açıklaması. |
| Tahsisat yöntemi | <p>Tahsisat yöntemini seçin:</p><ul><li>**Tamamlanma yüzdesi**: Her satır için toplam tamamlanma değeri kullanılır.</li><li>**Yüzde**: Tahsisat için bir yüzde tutarı belirtilebilir. Tüm yüzdelerin toplamı 100 olmalıdır.</li><li>**Değişken tutar**: Tahsisat için bir tutar belirtilebilir. Tahsisat tutarı hareket düzeyinde belirtilir.</li><li>**Eşit tutar**: Tahsisat yüzdeleri otomatik olarak hesaplanır ve şablondaki maddeler arasında eşit olarak bölünür.</li></ul> |
| Toplam süre | Şablon için kilometre taşı tutarını belirtin. |
| **Satırlar** | |
| Madde numarası | Kilometre taşı şablonu için madde numarasını seçin. |
| Ürün adı | Maddenin adı. |
| Yüzde | <p>Satır için tahsisat yüzdesini girin:</p><ul><li>**Tahsisat yöntemi** alanı **Yüzde** olarak ayarlanırsa satır için yüzdeyi belirtin.</li><li>**Tahsisat yöntemi** alanı **Eşit tutar** olarak ayarlanırsa yüzde, şablondaki madde sayısına göre otomatik olarak eşit yüzdelere bölünür.</li></ul><p>Tüm yüzdelerin toplamı 100 olmalıdır.</p><p>Üst bilgide **Toplam tutar** değeri belirtilirse ve satır için **Yüzde** değerini değiştirirseniz **Tutar** değeri güncelleştirilir. Aynı şekilde **Tutar** değerini değiştirirseniz **Yüzde** değeri güncelleştirilir.</p> |
| Tutar | <p>Satır için tahsisat tutarı:</p><ul><li>**Tahsisat yöntemi** alanı **Değişken tutar** olarak ayarlanırsa satır için tutarı belirtin.</li><li>**Tahsisat tutarı** alanı **Eşit tutar** olarak ayarlanırsa tutar şablondaki madde sayısı ve üst bilgide belirtilen **Toplam tutar** değerine göre otomatik olarak eşit tutarlara bölünür.</li></ul><p>Tüm tutarların toplamı, üst bilgide belirtilen **Toplam tutar** değerine eşit olmalıdır.</p><p>Üst bilgide **Toplam tutar** değeri belirtilirse ve satır için **Tutar** değerini değiştirirseniz **Yüzde** değeri güncelleştirilir. Aynı şekilde **Yüzde** değerini değiştirirseniz **Tutar** değeri güncelleştirilir.</p> |
| **Toplamlar** | |
| Toplam yüzde | Yüzde toplamı. Tüm yüzdelerin toplamı 100 olmalıdır. |
| Toplam süre | Tüm satırlar için **Tutar** değerlerinin toplamı. Bu toplam, üst bilgide belirtilen **Toplam tutar** değerine eşit olmalıdır. |
| Kalan tutar | Kalan tutar. Değer, üst bilgideki **Toplam tutar** değerinden tüm satırlar için **Tutar** değerleri toplamının çıkarılmasıyla hesaplanır.|

## <a name="milestone-allocation"></a>Kilometre taşı tahsisatı

Kilometre taşı işlevini kullanmaya başlamadan önce bu görevleri tamamlamanız gerekir.

1. Bir veya daha fazla kilometre taşı şablonu ekleyin.
2. Faturalama zamanlaması grubu oluşturun. Madde türü olarak **Kilometre taşı**'nı belirtin ve bir şablon seçin.
3. **Madde kurulumu** sayfasında (**Abonelik faturalaması \> Yinelenen sözleşme faturalaması \> Kurulum \> Maddeler**), madde kurulumu için bir madde ilişkisi ve bir kilometre taşı şablonu seçin.

Kilometre taşı şablonlarını, faturalama zamanlaması gruplarını ve maddeleri oluşturduktan sonra kilometre taşı işlevini kullanan bir faturalama zamanlaması oluşturabilirsiniz.

Kilometre taşlarını kullanan bir faturalama zamanlaması oluşturmak için bu adımları izleyin.

1. **Faturalama zamanlamaları** sayfasındaki **Tüm/Ekin faturalama zamanlamaları** listesinden **Yeni**'yi seçin.
2. **Tüm faturalama zamanlamaları** sayfasında yeni bir faturalama zamanlaması oluşturun ve bir müşteri hesabı ve başlangıç tarihi belirtin.
3. **Faturalama zamanlaması satırları** bölümünde **Satır ekle**'yi seçin. Ardından bir madde numarası ekleyin ve **Madde türü** alanını **Kilometre taşı** olarak ayarlayın.

    Madde için varsayılan bir kilometre taşı şablonu ayarlanırsa kilometre taşı olayları otomatik olarak faturalama zamanlaması satırlarına eklenir. Kilometre taşı satırları için bitiş tarihleri boştur.

    Madde için hiçbir kilometre taşı şablonu ayarlanmadıysa **Kilometre taşı tahsisatı**'nı seçin. Ardından **Kilometre taşı tahsisatı** sayfasında bir kilometre taşı şablonu seçin ve gerekli güncelleştirmeleri yapın. Ardından faturalama zamanlamasına dönmek için **Kapat**'ı seçin ve faturalama zamanlaması oluşturma işlemini tamamlayın.

4. Faturalama zamanlamasına yönelik faturalar oluşturmak için her bir kilometre taşı olayının bitiş tarihini güncelleştirmeniz gerekir. Tek bir faturalama zamanlaması için faturalama zamanlaması satırlarında kilometre taşı olayının bitiş tarihini güncelleştirebilirsiniz. Birden fazla faturalama zamanlamasını güncelleştirmek için **Tamamlanma tarihi işlemini güncelleştir**'i seçin.
5. Bitiş tarihi güncelleştirildikten sonra faturayı oluşturabilirsiniz. Tek bir faturalama zamanlaması için **Tüm faturalama zamanlamaları** sayfasında **Fatura oluştur**'u seçin. Birden fazla faturalama zamanlamasına yönelik faturalar oluşturmak için **Periyodik görevler** altında **Fatura oluştur**'u veya **Fatura oluşturma toplu işlemi**'ni seçin.

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Faturalama zamanlaması satırında kilometre taşı tahsisatını düzenleme

Faturalama zamanlaması satırında kilometre taşı tahsisatını düzenlemek için bu adımları izleyin.

1. **Faturalama zamanlamaları** sayfasında, > **Tüm veya etkin faturalama zamanlamaları** bölümünde **Zamanlama numarası** alanında faturalama zamanlamasının zamanlama numarasını seçin.
2. **Faturalama zamanlaması satırları** bölümüne bir madde girin, madde olarak **Kilometre taşı**'nı belirtin ve **Kilometre taşı tahsisatı**'nı seçin.
3. **Kilometre taşı şablonu** alanında, bir kilometre taşı şablonu seçin.
4. **İşlem**'i seçin. Kilometre taşı şablonu satırları, faturalama zamanlaması satırlarına otomatik olarak eklenir.

## <a name="milestone-allocation-fields"></a>Kilometre taşı tahsisatı alanları

**Kilometre taşı tahsisatı** sayfası, aşağıdaki alanları içerir.

| Alan | Açıklama |
|-------|-------------|
| Ana madde | Ana maddenin madde numarası. |
| Toplam fiyat | <p>Maddenin toplam fiyatı. Değer, faturalama zamanlaması satırının **Net tutar** değerine karşılık gelir.</p></p>Kilometre taşı ana maddesinin varsayılan değeri kilometre taşı şablonu için belirtilen **Toplam tutar** değeridir. Toplam tutar 0 (sıfır) ise varsayılan değer, faturalama zamanlaması satırının **Net tutar** değeridir.</p> |
| Kilometre taşı şablonu | Satır maddesinin kilometre taşı şablonu kimliği. |
| Şablon açıklaması | Kilometre taşı şablonunun açıklaması. |
| Tahsisat yöntemi | Kilometre taşı şablonu için kullanılan tahsisat yöntemi. |
| **Satırlar** | Tüm satırlar için varsayılan değerlerde seçili kilometre taşı şablonu temel alınır. Bunları gerektiği gibi değiştirebilirsiniz. |
| Madde numarası | Kilometre taşı tahsisat şablonu için madde numarası. |
| Ürün adı | Ürün adı. |
| Yüzde | <p>Satır için tahsisat yüzdesi. Tüm yüzdelerin toplamı 100 olmalıdır.</p><p>Satır için **Yüzde** değerini değiştirirseniz **Net tutar** değeri güncelleştirilir. Aynı şekilde **Net tutar** değerini değiştirirseniz **Yüzde** güncelleştirilir.</p> |
| Net tutar | <p>Satır için tahsisat tutarı. Tüm satırlar için net tutarların toplamı, üst bilgide belirtilen **Toplam fiyat** değerine eşit olmalıdır.</p><p>Satır için **Net tutar** değerini değiştirirseniz **Yüzde** değeri güncelleştirilir. Aynı şekilde **Yüzde** değerini değiştirirseniz **Net tutar** değeri güncelleştirilir.</p> |
| **Toplamlar** | |
| Toplam yüzde | Tüm satırlar için **Yüzde** değerlerinin toplamı. Bu toplam 100'e eşit olmalıdır. |
| Toplam süre | Tüm satırlar için **Net tutar** değerlerinin toplamı. Bu toplam, üst bilgide belirtilen **Toplam fiyat** değerine eşit olmalıdır. |
| Kalan tutar | Kalan tutar. Değer, üst bilgideki **Toplam fiyat** değerinden tüm satırlar için **Net tutar** değerleri toplamının çıkarılmasıyla hesaplanır. Nihai tutar 0 (sıfır) olmalıdır. |
