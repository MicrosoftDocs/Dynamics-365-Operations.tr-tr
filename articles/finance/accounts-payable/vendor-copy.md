---
title: Paylaşılan numara sıralarını kullanarak satıcıları kopyalama
description: Bu konuda, bir satıcıyı aynı satıcı kodunu koruyarak başka bir tüzel kişiliğe kopyalamak için paylaşılan numara sıralarının nasıl kullanılacağı açıklanmaktadır.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 33338c331a53586b325def398267ab10db23f78a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460104"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a>Paylaşılan numara sıralarını kullanarak satıcıları kopyalama

[!include [banner](../includes/banner.md)]

Satıcı kodları atamak için paylaşılan numara sıralarını kullanabilirsiniz. Paylaşılan numara sıraları, satıcıları bir tüzel kişilikten başka bir tüzel kişiliğe kopyalamanıza ve her iki tüzel kişilikte aynı satıcı kodlarını kullanmanıza da olanak tanır.

## <a name="setup"></a>Ayarlama

Özellik, satıcı kodları atamak için paylaşılan numara sırası kullandığınızda etkinleştirilir. Satıcıyı kopyalamak istediğiniz her tüzel kişilikte aynı numara sırasını kullanmanız gerekir. **Borç hesapları parametreleri** sayfasından her tüzel kişilik için satıcı numara sırasını değiştirebilirsiniz. **Borç hesapları** \> **Ayar** \> **Borç hesapları parametreleri**'ni ve ardından **Numara sıraları** sekmesini seçin.

Ayrıca, her satıcı grubu için satıcı numara sıraları ayarlayabilirsiniz. Bu numara sıralarının da paylaşılması gerekir. Öncelikle satıcı grubuna ilişkin numara sırası kullanılır. Satıcı grubu için numara sırası belirtilmediyse, **Borç hesapları parametreleri** sayfasında belirtilen numara sırası kullanılır.

Ayrıca, el ile satıcı kodları kullanıyorsanız satıcıları tüzel kişilikler arasında kopyalayabilirsiniz. Bununla birlikte, satıcıyı satıcı kodunun zaten bulunduğu bir tüzel kişiliğe kopyalamayı denerseniz, kopyalama işlemi başlatılmaz.

## <a name="copy-a-vendor"></a>Satıcı kopyalama

Bir satıcıyı kopyalamak için **Tüm satıcılar, yeni kayıt** sayfasını açmak üzere **Tüm satıcılar** liste sayfasında **Yeni**'yi seçin. Yeni satıcı kodunun hemen atanmayacağını unutmayın. Bu davranış, eski sürümlerdeki davranıştan farklıdır. Satıcı grubunu henüz seçmediğiniz için sistem kullanılacak doğru numara sırasını belirleyemez. Ayrıca, yeni bir satıcı oluşturmak mı yoksa bir satıcıyı kopyalamak mı istediğinizi de belirleyemez. Bu nedenle, satıcı kodu sayfanın alt kısmındaki **Kaydet** düğmesi seçilene kadar atanmaz.

Yeni bir satıcı oluşturuyorsanız, tüm alanları her zaman olduğu gibi doldurmaya devam edebilirsiniz. Tamamlayıp **Kaydet**'i seçtiğinizde, satıcı kodunun otomatik olarak atandığını görürsünüz. Alternatif olarak, el ile numara sıraları için el ile satıcı kodunuzun kullanıldığını görürsünüz.

Bir satıcıyı kopyalamak için **Ad** alanına aradığınız satıcıyı temsil eden bir veya daha fazla karakter girin. Bir arama iletişim kutusunda aradığınız satıcıyı temsil ediyor olabilecek tarafların listesi gösterilir. Taraflardan birini seçtiğinizde, iletişim kutusunun sağ tarafında ek bilgiler görüntülenir:

- **General** sekmesi tarafın telefon numarasını ve adresini gösterir.
- **Roller** sekmesi seçilen tarafın sahip olabileceği rolleri ve her role sahip olduğu tüzel kişiliği gösterir.
- **Vergi kaydı kodu** sekmesi tarafa atanmış olan vergi kaydı kodlarını gösterir.

Bir tarafı yalnızca bir satıcı rolüne sahip olması ve bu role geçerli tüzel kişilik dışındaki bir tüzel kişilikte sahip olması durumunda kopyalayabilirsiniz. Bu ölçütleri karşılayan bir taraf bulduğunuzda aşağıdaki adımları izleyin.

1. **Satıcıyı kopyala** seçeneği görüntülenir. Varsayılan olarak bu seçenek **Hayır** olarak ayarlanmıştır. Satıcıyı geçerli tüzel kişiliğe kopyalamak için seçeneği **Evet** olarak ayarlayın. 
2. **Tüzel kişilik** alanı görüntülenir. İçinden satıcıyı kopyalayacağınız tüzel kişiliği seçin. Satıcı yalnızca bir tüzel kişilikte yer alıyorsa, alan varsayılan olarak bu tüzel kişiliğe ayarlanır.
3. **Seç** öğesini seçin. Yeni satıcı oluşturulur.

## <a name="validation"></a>Doğrulama

Bir satıcıyı kopyaladığınızda, sistem yeni satıcı bilgilerini kaydetmeyi dener. Kopyalanan verilerin sağlam olduğundan emin olmak için doğrulamalar çalıştırılır. Başarısız olan her doğrulama için bir hata iletisi alırsınız. Hata iletileri hangi bilgilerin güncelleştirilmesi gerektiğini açıklar. Satıcının kopyası tüm doğrulama hataları düzeltilene kadar kaydedilemez.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Vergi muafiyet numarası arama özelliğini kullanarak bir satıcıyı kopyalama

**Tüm satıcılar** sayfasının Eylem Bölmesindeki **Satıcı** sekmesinde bulunan **Kayıt** grubundaki Vergi muafiyet numarası arama özelliğini kullanarak da satıcıları kopyalayabilirsiniz. Görüntülenen **Vergi muafiyet numarası arama** iletişim kutusu vergi muafiyet numaralarını, satıcı kodunu, satıcı adını ve vergi muafiyet kodunun kullanıldığı tüzel kişiliği gösterir. Bir satıcıyı yalnızca geçerli tüzel kişilik dışındaki bir tüzel kişilikte olması durumunda kopyalayabilirsiniz. Bu ölçütü karşılayan satıcıyı seçtikten sonra aşağıdaki adımları izleyin.

1. **Satıcıyı kopyala** seçeneği görüntülenir. Varsayılan olarak bu seçenek **Hayır** olarak ayarlanmıştır. Satıcıyı geçerli tüzel kişiliğe kopyalamak için seçeneği **Evet** olarak ayarlayın.
2. **Seç** öğesini seçin. Yeni satıcı oluşturulur.
