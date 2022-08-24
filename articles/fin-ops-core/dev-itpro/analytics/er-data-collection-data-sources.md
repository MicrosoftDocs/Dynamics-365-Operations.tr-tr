---
title: VERİ TOPLAMA veri kaynaklarını Elektronik raporlama biçimlerinde kullanma
description: Bu makalede, VERİ TOPLAMA veri kaynaklarının Elektronik raporlama (ER) biçimlerinde nasıl kullanılacağı açıklanmaktadır.
author: kfend
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.custom: 58771
ms.assetid: ''
ms.search.form: EROperationDesigner
ms.openlocfilehash: 221cefc1880cdd88a952140424daf24975a575aa
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286194"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>VERİ TOPLAMA veri kaynaklarını Elektronik raporlama biçimlerinde kullanma

[!include [banner](../includes/banner.md)]

Farklı biçimlerde giden belgeler oluşturmak için kullanılan bir ER çözümünün biçimini yapılandırmak için [Elektronik raporlama (ER)](general-electronic-reporting.md) çerçevesinin Operations tasarımcısını kullanabilirsiniz. Yapılandırılmış biçim bileşeninin hiyerarşik yapısı çeşitli türlerdeki biçim öğelerinden oluşur. Bu biçim öğeleri, oluşturulan belgeleri gerekli bilgilerle çalışma zamanında doldurmak için kullanılır. Varsayılan olarak, bir ER biçimini çalıştırdığınızda, biçim öğeleri, biçim hiyerarşisinde sunuldukları sırayla çalıştırılır: tek tek, üstten alta doğru.

ER, bir bağlama içeren bir biçim öğesini çalıştırdığında, bu bağlamanın formülü çalıştırılır ve biçim öğesi, değeri oluşturulan belgeye ekler. Örneğin, bağlama bir veri modeli alanının değerini bir biçim öğesine iletebilir. Çalışma zamanında veri modeli alanlarının değerlerini toplamak, değer toplama yapmak ve oluşturulan belgeyi toplanan değerlerle doldurmak için VERİ TOPLAMA veri kaynağı yapılandırabilirsiniz. Bu yaklaşımı kullanmak için yapılandırılan VERİ TOPLAMA veri kaynağının bir veri modeli alanının değerini, biçim öğesine geçirirken kullanılması için ilk bağlamayı değiştirin. VERİ TOPLAMA veri kaynağından değerleri geçirerek daha fazla kullanım için gerekli ayrıntıları toplayabilirsiniz.

VERİ TOPLAMA veri kaynağını yapılandırdığınızda, veri kaynağında yönetilecek bir değer türü belirtin. Aşağıdaki [veri türleri](er-formula-supported-data-types-primitive.md) şu anda değer toplamak için desteklenmektedir:

- Boole
- Date
- Tarih/Saat
- GUID
- Int64
- Tamsayı
- Gerçek
- Dize
- Saat

Toplama için veri kaynağına bir değeri geçirirken VERİ TOPLAMA veri kaynağının `Collect(Value)` yöntemini kullanabilirsiniz. Bu yöntemde, `Value` bağımsız değişkeni ilgili veri türünün veri kaynağı alanının sabit veya geçerli bir yoludur.

Toplanan değerler listesine erişmek için bir VERİ TOPLAMA veri kaynağının `Result` özelliğini kullanın. Bu özellik bir [kayıt listesi](er-formula-supported-data-types-composite.md#record-list) döndürür. Kayıt listesinin kayıtları, toplanan değerlere erişmek için kullanabileceğiniz `Value` alanını içerir.

Varsayılan olarak, VERİ TOPLAMA veri kaynağı yalnızca benzersiz değerler toplar.

Tüm değerleri toplamak için yapılandırılmış VERİ TOPLAMA veri kaynağının **Tüm değerleri topla** alanını **Evet** olarak ayarlayın. **Tüm değerleri topla** alanı **Evet** olarak ayarlandığında, `Sum(Flag)` parametreli özelliği kullanılabilir hale gelir. Şu anda toplanan tüm değerlerin toplam tutarını almak için bu özelliği kullanabilirsiniz. Bu özellikte, `Flag` bağımsız değişkeni, toplam değerin sıfırlanması gerekip gerekmediğini belirtmek için kullanılan bir [Boole](er-formula-supported-data-types-primitive.md#boolean) değeridir.

- **Yanlış** değeri sağlandığında, toplama işlemi daha önce toplanan tutardan devam eder.
- **Doğru** değeri sağlandığında yeni bir toplama işlemi başlatılır.

Şu anda toplama için aşağıdaki veri türleri desteklenmektedir:

- Int64
- Tamsayı
- Gerçek

Bu özellik hakkında daha fazla bilgi edinmek için aşağıdaki örneği tamamlayın.

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>Örnek: VERİ TOPLAMA veri kaynağı kullanarak sayma ve toplama yapmak için bir ER biçimini yapılandırma

Bu örnekte, Sistem yöneticisi veya Elektronik raporlama işlev danışmanı rolündeki bir kullanıcının, çalışan toplamları hesaplamak ve toplanan değerleri toplamak için kullanılan VERİ TOPLAMA veri kaynağına sahip bir ER biçimini nasıl yapılandırabileceğini gösterilmektedir.

Bu örnekteki prosedürler, Microsoft Dynamics 365 Finance'teki USMF şirketinde tamamlanabilir.

### <a name="upload-and-use-the-provided-er-solution"></a>Sağlanan ER çözümünü yükleme ve kullanma

1. [Örnek ER yapılandırmalarını içeri aktarma](er-defer-sequence-element.md#import-the-sample-er-configurations).
2. [Yapılandırma sağlayıcısı etkinleştirin](er-defer-sequence-element.md#activate-a-configurations-provider).
3. [İçeri aktarılan model eşlemesini inceleme](er-defer-sequence-element.md#review-the-imported-model-mapping).
4. [İçe aktarılan biçimi gözden geçirme](er-defer-sequence-element.md#review-the-imported-format).
5. [İçe aktarılan biçimi çalıştırma](er-defer-sequence-element.md#run-the-imported-format).

### <a name="run-the-format-of-the-provided-er-solution"></a>Sağlanan ER çözümünün biçimini çalıştırma

1. **Biçim tasarımcısı** sayfasında, **Çalıştır**'ı seçin.
2. **Elektronik rapor parametreleri** iletişim kutusunda **Tamam**'ı seçin.
3. Web tarayıcısının sunduğu dosyayı indirin ve inceleyin.

    ![İlk biçim yürütmenin sonuçlarını içeren indirilen dosya](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>Çalışan vergi toplamını hesaplamak için ER çözümünün biçimini değiştirme

İşlem hacmi, mevcut örnekteki hacimden çok daha büyükse toplamanın gerektirdiği süre artabilir ve performans sorunlarına neden olabilir. Biçimin ayarlarını değiştirerek bu performans sorunlarının önlenmesine yardımcı olabilirsiniz. Oluşturulan rapora dahil etmek üzere vergi değerlerine eriştiğiniz için vergi değerlerini toplamak için bu bilgileri yeniden kullanabilirsiniz.

1. **Biçim tasarımcısı** sayfasında, **Eşleme** sekmesinde **Kök ekle**'yi seçin.
2. **Veri kaynağı ekle** iletişim kutusunda, **İşlevler** \> **Veri toplama**'yı seçin.
3. **"Veri toplama" veri kaynağı özellikleri** iletişim kutusunda şu adımları izleyin:

    1. **Ad** alanına **CollectedTaxValues** girin.
    2. **Madde türü** alanında **Gerçek**'i seçin.
    3. **Tüm değerleri topla** alanında **Evet**'i seçin.
    4. **Tamam**'ı seçin.

4. **Rapor\\Satırlar\\Kayıt\\TaxAmount** sayısal biçim öğesini seçin.

    > [!NOTE]
    > Şu anda, bu öğe için `@.Value` bağlaması yapılandırılmıştır. Bu nedenle, `model.Data.List.Value` alanından vergi değerleri ile doldurulursa oluşturulan belge.

5. **Formül düzenle**’yi seçin.
6. **Formül tasarımcısı** sayfasında şu adımları izleyin:

    1. **Formül** alanında, `@.Value` değerini `CollectedTaxValues.Collect(@.Value)` ile değiştirin.
    2. Değişikliklerinizi kaydedin ve sayfayı kapatın.

    > [!NOTE]
    > Yeni bağlama, aynı vergi değerlerini oluşturulan belgeye geçirir. Ancak bu değerler **CollectedTaxValues** veri kaynağında da toplanır.

7. **Rapor\\Satırlar\\Kayıt\\RunningTotal** sayısal biçim öğesini seçin.
8. **Formül düzenle**’yi seçin.
9. **Formül tasarımcısı** sayfasında şu adımları izleyin:

    1. **Formül** alanına `CollectedTaxValues.Sum(false)` girin.
    2. Değişikliklerinizi kaydedin ve sayfayı kapatın.

    > [!NOTE]
    > Yeni bağlama, zaten girilmiş olan toplam vergi değerleri tutarını oluşturulan belgeye geçirir.

    ![Biçim tasarımcısı sayfasında güncelleştirilmiş bağlamaları olan sayısal öğeler](./media/er-data-collection-data-sources-02.png)

10. **Kaydet** i ve ardından **Çalıştır**'ı seçin.
11. **Elektronik rapor parametreleri** iletişim kutusunda **Tamam**'ı seçin.
12. Web tarayıcısının sunduğu dosyayı indirin ve inceleyin.

    ![Değiştirilmiş biçim yürütmesinin sonuçlarını içeren indirilen dosya](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>Toplanan vergi değerlerinin listesini değerlendirmek için biçimi değiştirme

1. **Format tasarımcısı** sayfasında, **Biçim** sekmesinde, **Rapor\\Satırlar\\Kayıt\\RunningTotal** sayısal biçim öğesini seçin ve ardından şu adımları izleyin:

    1. **Sayısal tür** alanında, **Gerçek** olan değeri **Tamsayı** olarak değiştirin.
    2. **Sayısal biçim** alanında, değeri **F2**'den **F0**'a değiştirin.

3. **Eşleme** sekmesinde, **Formül düzenle**'yi seçin.
4. **Formül tasarımcısı** sayfasında şu adımları izleyin:

    1. **Formül** alanına `COUNT(CollectedTaxValues.Result)` girin.
    2. Değişikliklerinizi kaydedin ve sayfayı kapatın.

    > [!NOTE]
    > Yeni bağlama, vergi değerlerinin toplandığı listedeki kayıt sayısını oluşturulan belgeye geçirir.

5. **Kaydet** i ve ardından **Çalıştır**'ı seçin.
6. **Elektronik rapor parametreleri** iletişim kutusunda **Tamam**'ı seçin.
7. Web tarayıcısının sunduğu dosyayı indirin ve inceleyin.

    ![Başka bir değiştirilmiş biçim yürütmesinin sonuçlarını içeren indirilen dosya](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>Çalışan toplamları hesaplamam ve veri toplamam gerekiyorsa VERİ TOPLAMA veri kaynağı kullanmayla yerleşik VERİ TOPLAMA işlevlerini kullanma arasındaki fark nedir?

Hem VERİ TOPLAMA veri kaynağı hem de yerleşik [VERİ TOPLAMA](er-functions-category-data-collection.md) işlevleri, oluşturulan bir giden belgeye geçirilen bilgilere göre veri toplama, toplama ve sayım işlemlerini yapmak için kullanılabilir. Ancak hangi tekniği kullanacağınıza karar vermeye çalışırken aşağıdaki noktaları dikkate alın.

| Veri kaynağı | Yerleşik işlevler |
|-------------| ------------------ |
| Yalnızca değerler toplanır. | <p>Adlandırılmış değerler toplanır. Bu nedenle, ayrı değer grupları için toplamlar hesaplanabilir.</p><p>Ek olarak, gruplar bir liste olarak ayıklanabilir.</p><p>Metin değerleri de toplanabilir.</p> |
| Benzersiz değerler otomatik olarak toplanır. | Toplanan değerlerden benzersiz değerlerin listesini ayıklamak için ek ayarlar gerekir. |
| Performans, toplanan değerlerin hacmine bağlıdır. | Uygulamada performans, toplanan değerlerin hacmine bağlı değildir. |
| Bu teknik, her tür giden belge için geçerlidir. | Bu teknik yalnızca metin ve XML belgeleri için geçerlidir. |

## <a name="additional-resources"></a>Ek kaynaklar

- [Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma](./tasks/er-format-counting-summing-1.md)
- [ER biçimindeki sıra öğelerinin yürütülmesini erteleme](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
