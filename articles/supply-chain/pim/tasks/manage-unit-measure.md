---
title: Ölçü birimlerini yönetme
description: Bu konu; bir ölçü birimi tanımlamayı, bu birim ve açıklaması için çeviriler oluşturmayı ve ilgili birimler için dönüştürme kuralları tanımlamayı gösterir.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d251f90675188426e74b8cbe672856eb4c9ecb8a391f54e735ba19b91b7e3f4a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746951"
---
# <a name="manage-units-of-measure"></a>Ölçü birimlerini yönetme

[!include [banner](../../includes/banner.md)]

Bu konu; bir ölçü birimi tanımlamayı, bu birim ve açıklaması için çeviriler oluşturmayı ve ilgili birimler için dönüştürme kuralları tanımlamayı gösterir.

## <a name="open-the-units-page"></a>Birimler sayfasını açma

Sisteminizde kullanılabilen ölçü birimlerini oluşturmak ve bunlarla çalışmak için **Kuruluş Yönetimi \> Kurulum \> Birimler \>Birimler**'e gidin.

Bu konunun geri kalan bölümleri, **Birimler** sayfasında neler yapabileceğinizi açıklamaktadır.

## <a name="create-standard-units-and-conversions"></a>Standart birimler ve dönüşümler oluşturma

Sisteminiz metrik sistem ve/veya ABD geleneksel sistemi (USCS) için en sık kullanılan ölçü birimlerini içermiyorsa, birim kurulum sihirbazı, temel birim tanımları ve dönüştürmelere hızlı şekilde başlamanıza yardımcı olabilir. Sihirbazı tamamlamak için, Eylem Bölmesinde **Birim oluşturma sihirbazı**'nı seçin ve sonra ekrandaki talimatları izleyin.

## <a name="create-or-edit-a-unit-of-measure"></a>Bir ölçü birimi oluşturma veya düzenleme

Bir ölçü birimi oluşturmak veya düzenlemek için aşağıdaki adımları izleyin.

1. Şu adımlardan birini izleyin:

    - Varolan bir birimi düzenlemek için, birimi liste bölmesinde seçin.
    - Yeni bir birim oluşturmak için Eylem Bölmesinde **Yeni**'yi seçin.

1. Kaydın üst bilgisinde aşağıdaki alanları ayarlayın:

    - **Birim** – Sistem dilinde birime başvuruda bulunmak için kullanılacak kodu veya simgeyi girin. Bu kod veya simge genellikle birim için ortak bir kısaltmadır (örneğin, her biri için *beher* veya santimetre için *cm*).
    - **Açıklama** – Sistem dilinde birim için açıklayıcı bir ad girin. Bu ad genellikle birimin tam adıdır. Örneğin *Her biri* veya *Santimetre* gibi.

1. **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın:<!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - **Birim sınıfı** – Birimin ölçtüğü özelliği seçin (uzunluk, alan, kütle veya miktar gibi).
    - **Birim sistemi** – Birimin ait olduğu ölçü sistemini seçin (*Metrik birimler* veya *Amerika Birleşik Devletleri geleneksel birimler*).
    - **Temel birim** – Birim sınıfı için temel birim olarak geçerli birimi kullanmak için bu seçeneği *Evet* olarak ayarlayın. Bu durumda, temel birim ve birim sınıfındaki her ek birim arasında dönüştürme faktörünü belirtmeniz yeterlidir. Sistem daha sonra bu birim sınıfındaki tüm birimler arasında dönüştürme yapabilir. Bu nedenle, dönüşümleri ayarlamak daha kolaydır.

        Örneğin, galon, *Hacim* birim sınıfının taban birimiyse, litreden galona ve pintten galona dönüştürme faktörlerini ayarlamanız yeterli olacaktır. Sistem ardından litreden pinte dönüşümü gerçekleştirebilir.

        Her birim sınıfı için yalnızca bir temel birime sahip olabilirsiniz.

    - **Sistem birimi** – Birim sınıfında belirlenmemiş tüm ölçümler için varsayılan birim olarak geçerli birimi kullanmak için bu seçeneği *Evet* olarak ayarlayın. Örneğin, bir miktar girmek için kullanılan bir alan bir birimin belirtilmesine izin vermiyorsa (veya kullanıcı bir birim seçmezse), sistem *Miktar* birim sınıfı için sistem birimi olarak ayarlanan birimi kullanır . Her birim sınıfı için yalnızca bir sistem birimine sahip olabilirsiniz.
    - **Ondalık duyarlık** – Geçerli birim için belirtilen veya kendisine dönüştürülen değerlerin yuvarlanacak ondalık basamak sayısını belirtin.

1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="define-unit-translations"></a>Birim çevirilerini tanımlayın

Kod veya simge için çeviriler ve ölçü biriminin açıklamasını tanımlamak için aşağıdaki adımları izleyin.

1. Çevirileri oluşturmak için birim oluşturun veya seçin.
1. Eylem Bölmesi'nde, **Birim metinleri**'ni seçin.

    **Birim metinleri** sayfası görüntülenir. Seçili birimin kimliğine veya simgesine ait çevirileri tanımlamak için bu sayfayı kullanın. Daha sonra bu çeviriler müşteriye özgü veya satıcıya özgü dillerdeki harici belgelerde kullanılabilir.

1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Dil** alanında, birim kimliği veya simgesinin çevrileceği dili seçin.
1. **Metin** alanında, seçilen dilde birim kodunun veya sembolün çevirisini girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Sayfayı kapatın.
1. **Eylem Bölmesi**'nde, **Çevrilmiş birim açıklamaları**'nı seçin.

    **Çevrilen birim açıklamaları** sayfası görüntülenir. Bu sayfayı, seçili birimin dile özgü açıklamalarını tanımlamak için kullanırsınız.

1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Dil** alanında, birim açıklamasının çevrileceği dili seçin.
1. **Açıklama** alanında, seçilen dilde birim açıklamasının çevirisini girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Sayfayı kapatın.

## <a name="define-unit-conversion-rules"></a>Birim dönüştürme kurallarını tanımlayın

Ölçü birimleri arasında dönüştürmelere yönelik kurallar tanımlamak için aşağıdaki adımları izleyin.

1. Dönüştürme kuralları için birim oluşturun veya seçin.
1. Eylem Bölmesi'nde, **Birim dönüşümleri**'ni seçin.

    **Birim dönüştürmeleri** sayfası görüntülenir. Bu sayfayı kullanarak seçili birimi birim sınıfında bir başka ölçü birimine dönüştürmek için kurallar tanımlayın.

1. Ayarlamak istediğiniz dönüştürme türüne bağlı olarak aşağıdaki sekmelerden birini seçin:

    - **Standart dönüştürmeler** – Tüm ürünler için standart dönüştürme kuralları ayarlayın.
    - **Sınıf içi dönüştürmeler** – Aynı birim sınıfındaki birimler için ürüne özgü dönüştürme kuralları ayarlayın.
    - **Sınıf arası dönüştürmeler** – Birim sınıfları arasındaki birimler için ürüne özgü dönüştürme kuralları ayarlayın.

1. Şu adımlardan birini izleyin:

    - Yeni bir dönüştürme oluşturmak için araç çubuğunda **Yeni**'yi seçin.
    - Varolan bir dönüştürmeyi düzenlemek için, ızgarada dönüştürmeyi seçin ve araç çubuğundan **Düzenle**'yi seçin.

1. Görüntülenen açılır iletişim kutusunda aşağıdaki alanları ayarlayın:

    - **Ürün** - Dönüştürmenin uygulandığı belirli ürünü seçin. Bu alan yalnızca sınıf içi ve sınıf arası dönüştürmeler için kullanılabilir.
    - **Formül düzeni** – Tek etmene sahip basit bir dönüştürme belirtmek için bu alanı *Basit* olarak ayarlayın. Daha karmaşık bir denklem ayarlamak için bunu *Gelişmiş* olarak ayarlayın. Gelişmiş denklemler biçimi, birim sınıfa bağlı olarak değişir.
    - **Kaynak birim** – Bu alan, seçilen birimi gösterir. Genellikle, değeri değiştirmemelisiniz. (Değeri değiştirirseniz, kaydettikten sonra yeni dönüştürmeyi görüntülemek için seçili birime ait **Birim dönüştürmeleri** sayfasını kullanabilirsiniz.)
    - **Hedef birim** – Dönüştürülecek birimi seçin.
    - **Yuvarlama** – Kesirlerin, seçilen birimin **Ondalık duyarlık** değerine ( *En yakına*, *Yukarı* veya *Aşağı*) göre nasıl yuvarlanacağını seçin.
    - **Dönüştürme formülü** – İki birim arasındaki dönüştürme formülü belirtmek için açılır iletişim kutusunun üst kısmındaki kalan alanları kullanın. Kullanılabilir alanlar, seçtiğiniz birim sınıfına ve formül düzenine göre değişir.

1. **Tamam**'ı seçin.
1. Sayfayı kapatın.

> [!TIP]
> Ayrıca, her bir ürün varyantı için birim dönüştürmeleri ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Ürün çeşidi başına ölçü birimi dönüşümü](../uom-conversion-per-product-variant.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
