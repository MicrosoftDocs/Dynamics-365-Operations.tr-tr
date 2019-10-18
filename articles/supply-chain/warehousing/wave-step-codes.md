---
title: Dalga adım kodları
description: Bu konu altında, dalga adımı kodları hakkında genel bilgi ve bu kodların nasıl kullanıldığı açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992369"
---
# <a name="wave-step-codes"></a>Dalga adım kodları

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a>Dalga adımı kodları hakkında

Dalga adımı kodları, kullanıcıların, dalga yöntemlerinin belirli örneklerini ilgili bir şablona bağlamak için ayarlayıp kullanabileceği kodlardır. Şablonlar, stok yenileme, konteyner kullanımı, etiket yazdırma, yük oluşturma ve sıralama şablonlarını içerir.

Dalga adımı kodları kullanılmadığı zaman, kullanıcıların dalga yöntemi örneğinden belirli bir şablona başvuruda bulunmak için serbest metin girmeleri gerekir. Serbest metin hataya açıktır çünkü kullanıcılar bir dalga şablonunda belirli bir dalga adımı yöntemi için ekledikleri dalga adımı metninin, hedef şablondaki dalga adımı metniyle tam olarak eşleştiğinden emin olmalıdır.

Belirli bir dalga adımı türü için dalga adımı kodları ayrı bir sayfada ayarlanır. Dalga adımı kodu gerektiren bir dalga şablonunda bulunan her bir dalga adımı yöntemi örneği için, dalga adımı kodunun açılan listede seçilmesi gerekir. Açılır listedeki seçim serbest metin girişinin yerini alır ve insan hatası riskini ve etkisini azaltmaya yardımcı olur. Kurulum kodları, bir dalga şablonundaki dalga adımı yöntemini yöntem için hedef şablona bağlamak amacıyla kullanılır.

> [!NOTE]
> Dalga adımı kodları özelliğinin kullanımı isteğe bağlıdır ve tüzel kişilik için yükseltme yapılır. Bu nedenle, belirli bir tüzel kişilik bu özelliği kullanıyorsa, o tüzel kişilikteki tüm varolan dalga adımı kodları yeni yapıya yükseltilir.

## <a name="setup-demo"></a>Kurulum demosu 

Bu demo için, demo verilerinin yüklenmiş olması ve **USMF** demo veri şirketini kullanmanız gerekir.

### <a name="enable-wave-step-codes"></a>Dalga adım kodlarını etkinleştir

Dalga adımı kodları özelliğini açmak için bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
2. **Genel** sekmesinde **Dalga işleme** hızlı sekmesindeki **Dalga adımı kodlarını etkinleştir** seçeneğini **Evet** olarak ayarlayın.

Varolan tüm dalga adımı serbest metinleri yeni yapıya yükseltilir. Bir tüzel kişilik için bu yükseltme işlemi tamamlandıktan sonra, **Ambar yönetimi parametreleri** sayfasında **Dalga adımı kodlarını etkinleştir** seçeneği artık kullanılamaz.

Yükseltme sırasında doğrulamalar yapılır ve yükseltme başarısız olursa bir hata iletisi alırsınız. Bir yükseltme aşağıdaki çakışmalar nedeniyle başarısız olabilir:

- Tekrarlanan dalga adımı serbest metinleri vardır.
- Özelleştirmeler vardır.
- Bir dalga adımı yöntemi örneğiyle ilişkilendirilmiş dalga adımı serbest metni, beklenen şablon türüyle eşleşmiyordur.

Doğrulamalar sırasında tanımlanan çakışmaları çözümledikten sonra yükseltme işlemini yeniden çalıştırabilirsiniz.

Yükseltme başarılı olursa **Dalga adımı kodları** sayfası (**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga adımı kodları**) kullanılabilir duruma gelir. Dalga adımı kodları özelliği açıksa, bu sayfada, yükseltilmiş dalga adımı kodları listelenir.

### <a name="create-new-wave-step-codes"></a>Yeni dalga adımı kodları oluşturma

Dalga adımı kodları oluşturmak ve silmek için **Dalga adımı kodları** sayfasını kullanabilirsiniz.

Her yeni dalga adımı kodu ve ilişkili kodu, tüm dalga adımı türleri arasında benzersiz olmalıdır ve belirli bir dalga adımı türü için tanımlanmalıdır.

### <a name="apply-wave-step-codes"></a>Dalga adımı kodlarını uygulama

Siz uygun dalga adımı kodlarını tanımladıktan sonra bu kodlar dalga işlemi yöntemlerine uygulanabilir.

Dalga adımı kodlarını uygulamak için uygun hedef şablonuna gidin. Dalga adımı kodlarının işaret etmek üzere belirlenmiş olduğu hedef şablonlar:

- **Stok yenileme şablonları:** Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları
- **Yük oluşturma şablonları:** Ambar yönetimi \> Kurulum \> Yük \> Yük oluşturma şablonları
- **Sıralama şablonları:** Ambar yönetimi \> Kurulum \> Ambalaj \> Giden sıralama şablonları
- **Konteyner kullanımı şablonları:** Ambar yönetimi \> Kurulum \> Konteynerler \> Konteyner yapı şablonları
- **Etiket yazdırma şablonları:** Ambar yönetimi \> Kurulum \> Belge rotası \> Dalga etiketi şablonları

Bu listedeki şablonlar, bir dalga şablonunda seçilen bir dalga işlemi yönteminden başvurulduğunda uygulanır. Bir dalga şablonunda dalga işleme yöntemindeki dalga adımı kodu, şablon türlerinden birindeki dalga adım koduyla eşleştiğinde şablon uygulanır.

### <a name="sample-scenario"></a>Örnek senaryo

Aşağıdaki yordam, oluşturduğunuz stok yenileme şablonunun dalga şablonu için uygulanmasını garantilemeye yardımcı olur.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga adımı kodları**'na gidin ve **Stok yenileme** türü için bir dalga adımı kodu oluşturun.
2. **Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları**'na gidin ve bir stok yenileme şablonu oluşturun.
3. Stok yenileme şablonunda, **Stok yenileme** türü için oluşturduğunuz dalga adımı kodunu seçin.
4. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin ve kullanmayı düşündüğünüz dalga şablonunu seçin.
5. Şablonda, **Yöntemler** hızlı sekmesinde **Stok yenileme** yöntemini seçin.
6. **Dalga adımı kodu** alanında, stok yenileme şablonunda seçtiğiniz dalga adımı kodunu seçin.