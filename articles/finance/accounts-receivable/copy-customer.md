---
title: Paylaşılan numara sıralarını kullanarak müşterileri kopyalama
description: Bu konuda, bir müşteriyi aynı müşteri kodunu koruyarak başka bir tüzel kişiliğe kopyalamak için paylaşılan numara sıralarının nasıl kullanılacağı açıklanmaktadır.
author: mikefalkner
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: d906ed3cb7af0af9e0137f878c39d5ad47616a783688ad70b1465bd0b2d470aa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763346"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a>Paylaşılan numara sıralarını kullanarak müşterileri kopyalama

[!include [banner](../includes/banner.md)]

Müşteri kodları atamak için paylaşılan numara sıralarını kullanabilirsiniz. Paylaşılan numara sıraları, müşterileri bir tüzel kişilikten başka bir tüzel kişiliğe kopyalamanıza ve her iki tüzel kişilikte aynı müşteri kodlarını kullanmanıza da olanak tanır.

## <a name="setup"></a>Ayarlama

Özellik, müşteri kodları atamak için paylaşılan numara sırası kullandığınızda etkinleştirilir. Müşteriyi kopyalamak istediğiniz her tüzel kişilikte aynı numara sırasını kullanmanız gerekir. **Alacak hesapları parametreleri** sayfasından her tüzel kişilik için müşteri numara sırasını değiştirebilirsiniz. **Alacak hesapları** \> **Parametreler**'i ve ardından **Numara sıraları** sekmesini seçin.

Ayrıca, her müşteri grubu için müşteri numara sıraları ayarlayabilirsiniz. Bu numara sıralarının da paylaşılması gerekir. Öncelikle müşteri grubuna ilişkin numara sırası kullanılır. Müşteri grubu için numara sırası belirtilmediyse, **Alacak hesapları parametreleri** sayfasında belirtilen numara sırası kullanılır.

Ayrıca, el ile müşteri kodları kullanıyorsanız müşterileri tüzel kişilikler arasında kopyalayabilirsiniz. Bununla birlikte, müşteriyi müşteri kodunun zaten bulunduğu bir tüzel kişiliğe kopyalamayı denerseniz, kopyalama işlemi başlatılmaz.

## <a name="copy-a-customer"></a>Müşteriyi kopyalama

Bir müşteriyi kopyalamak için **Tüm müşteriler** liste sayfasında **Yeni**'yi seçerek **Müşteri oluştur** iletişim kutusunu açın. Yeni müşteri kodunun hemen atanmayacağını unutmayın. Bu davranış, eski sürümlerdeki davranıştan farklıdır. Müşteri grubunu henüz seçmediğiniz için sistem kullanılacak doğru numara sırasını belirleyemez. Ayrıca, yeni bir müşteri oluşturmak mı yoksa bir müşteriyi kopyalamak mı istediğinizi de belirleyemez. Bu nedenle, müşteri kodu iletişim kutusunun alt kısmındaki **Kaydet** düğmesi seçilene kadar atanmaz.

Yeni bir müşteri oluşturuyorsanız, tüm alanları her zaman olduğu gibi doldurmaya devam edebilirsiniz. Tamamlayıp **Kaydet**'i seçtiğinizde, müşteri kodunun otomatik olarak atandığını görürsünüz. Alternatif olarak, el ile numara sıraları için el ile müşteri kodunuzun kullanıldığını görürsünüz.

Bir müşteriyi kopyalamak için **Ad** alanına aradığınız müşteriyi temsil eden bir veya daha fazla karakter girin. Bir arama iletişim kutusunda aradığınız müşteriyi temsil ediyor olabilecek tarafların listesi gösterilir. Taraflardan birini seçtiğinizde, iletişim kutusunun sağ tarafında ek bilgiler görüntülenir:

- **General** sekmesi tarafın telefon numarasını ve adresini gösterir.
- **Roller** sekmesi seçilen tarafın sahip olabileceği rolleri ve her role sahip olduğu tüzel kişiliği gösterir.
- **Vergi kaydı kodu** sekmesi tarafa atanmış olan vergi kaydı kodlarını gösterir.

Bir tarafı yalnızca bir müşteri rolüne sahip olması ve bu role geçerli tüzel kişilik dışındaki bir tüzel kişilikte sahip olması durumunda kopyalayabilirsiniz. Bu ölçütleri karşılayan bir taraf bulduğunuzda aşağıdaki adımları izleyin.

1. **Müşteriyi kopyala** seçeneği görüntülenir. Varsayılan olarak bu seçenek **Hayır** olarak ayarlanmıştır. Müşteriyi geçerli tüzel kişiliğe kopyalamak için seçeneği **Evet** olarak ayarlayın. 
2. **Tüzel kişilik** alanı görüntülenir. İçinden müşteriyi kopyalayacağınız tüzel kişiliği seçin. Müşteri yalnızca bir tüzel kişilikte yer alıyorsa, alan varsayılan olarak bu tüzel kişiliğe ayarlanır.
3. **Seç** öğesini seçin. Yeni müşteri oluşturulur.

## <a name="validation"></a>Doğrulama

Bir müşteriyi kopyaladığınızda, sistem yeni müşteri bilgilerini kaydetmeyi dener. Kopyalanan verilerin sağlam olduğundan emin olmak için doğrulamalar çalıştırılır. Başarısız olan her doğrulama için bir hata iletisi alırsınız. Hata iletileri hangi bilgilerin güncelleştirilmesi gerektiğini açıklar. Müşterinin kopyası tüm doğrulama hataları düzeltilene kadar kaydedilemez.

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a>Vergi muafiyet numarası arama özelliğini kullanarak bir müşteriyi kopyalama

**Tüm müşteriler** sayfasının Eylem Bölmesindeki **Müşteri** sekmesinde bulunan **Kayıt** grubundaki Vergi muafiyet numarası arama özelliğini kullanarak da müşterileri kopyalayabilirsiniz. Görüntülenen **Vergi muafiyet numarası arama** iletişim kutusu vergi muafiyet numaralarını, müşteri kodunu, müşteri adını ve vergi muafiyet kodunun kullanıldığı tüzel kişiliği gösterir. Bir müşteriyi yalnızca geçerli tüzel kişilik dışındaki bir tüzel kişilikte olması durumunda kopyalayabilirsiniz. Bu ölçütü karşılayan müşteriyi seçtikten sonra aşağıdaki adımları izleyin.

1. **Müşteriyi kopyala** seçeneği görüntülenir. Varsayılan olarak bu seçenek **Hayır** olarak ayarlanmıştır. Müşteriyi geçerli tüzel kişiliğe kopyalamak için seçeneği **Evet** olarak ayarlayın. 
2. **Seç** öğesini seçin. Yeni müşteri oluşturulur.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]