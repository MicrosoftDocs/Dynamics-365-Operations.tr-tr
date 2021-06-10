---
title: Mobil cihaz kullanıcı ayarları
description: Bu konuda, ambar çalışanları için mobil cihaz kullanıcı ayarlarının nasıl yönetileceği açıklanmaktadır.
author: MarkusFogelberg
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mafoge
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 77b4276cec5e046a19d6d001acf41fc410052fba
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049304"
---
# <a name="mobile-device-user-settings"></a>Mobil cihaz kullanıcı ayarları

[!include [banner](../../includes/banner.md)]

Yeni Ambar Yönetimi mobil uygulaması, kullanıcı deneyimini uyarlamaya yardımcı olan uygulamaya özgü bir dizi ayara sahiptir. Uygulama farklı ekran boyutlarında ve yapılandırmalarda (tablet, telefon veya kola takılan cihaz gibi) kullanılabildiğinden, bu ayarları Microsoft Dynamics 365 Supply Chain Management'tan merkezi olarak yönetmek yararlı olabilir.

*Mobil cihaz kullanıcı ayarları* özelliği, tüm cihazlarda kullanılacak genel kullanıcı ayarlarını tanımlamanızı sağlar. Ayrıca, tek tek cihaz markaları, cihaz modelleri ve/veya çalışanlar için daha ayrıntılı kullanıcı ayarları tanımlayabilirsiniz. Bir çalışan Ambar Yönetimi mobil uygulamasında oturum açtığında, uygulama eşleşen marka, cihaz ve/veya kullanıcı kimliği için Supply Chain Management'ta depolanan özel ayarlar profilini getirir ve uygular.

Bu özellik, çalışanların yeni bir cihaz kullanmaya başladıklarında daha hızlı başlamalarına yardımcı olabilir. Burada bazı örnekler verilmiştir:

- Yöneticiler, belirli bir üreticinin cihazları ve/veya belirli cihaz modelleri için en iyi şekilde çalışan standart bir tercihler kümesi oluşturabilir. Bu nedenle, çalışanlar ayarları değiştirmek zorunda kalmadan yeni bir cihazı kullanmaya başlayabilir.
- Şirketinizde çalışanlar arasında paylaşılan aynı cihazlardan oluşan bir havuz varsa çalışanlar belirli bir günde seçtikleri belirli bir fiziksel cihazı hiç kullanmamış olsalar bile, her oturum açtıklarında tercih ettikleri kurulumu görürler.
- Supply Chain Management'ta yöneticiler, tek tek çalışanlar için bile depolanan tüm ayarları görüntüleyebilir ve düzenleyebilir. Bu özellik, yeni özelliklerde sorun gidermelerine veya ince ayar yapmalarına yardımcı olabilir.

> [!IMPORTANT]
> *Mobil cihaz kullanıcı ayarları* özelliği yalnızca yeni Ambar Yönetimi mobil uygulaması için geçerlidir. Eski ambar uygulamasıyla çalışmaz.

## <a name="turn-on-the-mobile-device-user-settings-feature"></a>Mobil cihaz kullanıcı ayarları özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Yeni ambar uygulaması için kullanıcı ayarları, simgeler ve adım başlıkları*

## <a name="create-and-manage-user-settings"></a>Kullanıcı ayarları oluşturma ve yönetme

Tüm parçalı yapı düzeylerinde ayar profilleri oluşturmak, görüntülemek ve yönetmek için **Mobil cihaz kullanıcı ayarları** sayfasını kullanın. Bir çalışan yeni bir cihazda kullanıcı ayarlarını ilk kez düzenlediğinde, zaten yoksa bu sayfaya otomatik olarak yeni bir profil eklenir. Bu profil daha sonra çalışan her değişiklik yaptığında güncelleştirilir.

Tüm cihaz markaları, cihaz modelleri ve/veya çalışanlar için geçerli olan bir ayar profili de tanımlayabilirsiniz. Daha sonra, tek tek markalar, modeller ve/veya çalışanlar için daha fazla özel ayar uygulayarak ayrıntı düzeyini artırabilirsiniz.

Mobil cihazlarınız için kullanıcı ayarları oluşturmak ve yönetmek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Mobil cihaz \> Mobil cihaz kullanıcı ayarları**'na gidin.
1. Kaydını açmak için liste bölmesinde var olan bir kullanıcı ayarları profilini seçin. Alternatif olarak yeni bir profil oluşturmak için eylem bölmesinde **Yeni**'yi seçin.

    Liste bölmesindeki her profil, profilin uygulandığı markayı, modeli ve/veya kullanıcı kimliğini belirtmek için etiketlenmiştir. Daha genel profiller, bu özelliklerin bazıları veya tümü için *Tümü* değerine sahiptir.

1. Yeni veya seçilen ayarlar profili kaydının başlık bölümünde, aşağıdaki alanları ayarlayın:

    - **Cihaz markası adı**: Profilin geçerli olması gereken cihaz markası adını seçin. Profilin tüm markalar için geçerli olması gerekiyorsa bu alanı boş bırakın. Değerler listesi, sisteminizde tanımlanan tüm markaları içerir. Marka listesinin nasıl tanımlanacağı hakkında bilgi için sonraki bölüme bakın.
    - **Cihaz modeli kimliği**: Profilin geçerli olması gereken cihaz modelini seçin. Profilin seçili markanın tüm modelleri için geçerli olması gerekiyorsa bu alanı boş bırakın. Değerler listesi, **Cihaz markası adı** alanında seçilen marka için tanımlanan tüm modelleri içerir. Her markanın model listesini tanımlama hakkında bilgi için bir sonraki bölüme bakın.
    - **Kullanıcı Kimliği**: Ayar profilinin geçerli olması gereken ambar çalışanının kullanıcı kimliğini seçin. Profilin tüm çalışanlar için geçerli olması gerekiyorsa bu alanı boş bırakın.

1. **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Düğme konumu**: Düğmelerin cihazda nasıl konumlandırılacağını seçin. Uygulamadaki öğeler, çalışanın tercihine veya kullandığı ele daha iyi uyacak şekilde taşınacaktır. Kullanılabilir seçenekler *Alt sağ (varsayılan)*, *Alt sol*, *Sağ üst* ve *Sol üst* seçenekleridir.
    - **Görüntü yönü**: Uygulamada varsayılan olarak geçerli olması gereken görüntü yönünü seçin.
    - **Kamerayla tara**: Tercih edilen giriş modunun *Tarama* olarak ayarlandığı giriş alanlarını taramak amacıyla cihaz kamerasını kullanmak için bu seçeneği *Evet* olarak ayarlayın. Cihazınızda yerleşik bir tarayıcı varsa bunun yerine tarayıcıyı kullanmak için bu seçeneği *Hayır* olarak ayarlayın.
    - **Ürün fotoğrafını göster**: Piyasaya sürülen ürünün ürün fotoğrafları mevcutsa gösterilip gösterilmeyeceğini seçin. Ürün resimlerini ekleme hakkında daha fazla bilgi için bkz. [Ürüne resim ekleme](../pim/tasks/add-image-product.md).
    - **Renk temasını görüntüle**: Cihaz için bir renk teması seçin.
    - **Ses düzeyi**: Cihaz için ses düzeyi seçin. 0 (sıfır) ile 10 arasında bir değer seçin. *0* değeri ses olmama durumunu ve *10* değeri en fazla ses düzeyini temsil eder. Varsayılan değer *4* şeklindedir.
    - **Titreşim düzeyi**: Cihaz için titreşim düzeyi seçin. 0 (sıfır) ile 5 arasında bir değer seçin. *0* değeri titreşim olmama durumunu ve *5* değeri en fazla titreşim düzeyini temsil eder. Varsayılan değer *1* şeklindedir.
    - **Metin ölçeği yüzdesi**: Metin boyutunu standart boyutun yüzdesi olarak belirtin. 70 ile 400 arasında bir değer girin. *70* değeri en küçük metin ölçeğini, *400* değeri ise en büyük metin ölçeğini temsil eder. Varsayılan değer *100* şeklindedir.
    - **Düğme ölçeği yüzdesi**: Düğme boyutunu standart boyutun yüzdesi olarak belirtin. 50 ile 200 arasında bir değer girin. *50* değeri en küçük düğme ölçeğini, *200* değeri ise en büyük düğme ölçeğini temsil eder. Varsayılan değer *100* şeklindedir.

## <a name="create-and-manage-mobile-device-brands"></a>Mobil cihaz markaları oluşturma ve yönetme

Ayar profillerinizle kullanılabilecek cihaz markalarını ve modellerini görüntülemek, oluşturmak ve yönetmek için **Mobil cihaz markaları** sayfasını kullanın. Mobil uygulama, bir çalışanın belirli bir cihazda ayarlarını ilk kez düzenlediğinde yerel marka adını ve model adını otomatik olarak getirir ve gönderir. Bu nedenle, bu kayıtların çoğu genellikle otomatik olarak oluşturulur. Ancak bu sayfadaki tüm kayıtları da yönetebilirsiniz. Örneğin, benzer veya şifreli model kimliklerini ayırt etmeye yardımcı olmak için her marka ve modele daha yararlı açıklamalar verebilirsiniz.

Mobil cihaz markalarınızı ve modellerinizi oluşturmak ve yönetmek için bu adımları izleyin.

1. **Ambar yönetimi \> Mobil cihaz \> Mobil cihaz markaları**'na gidin.
1. Liste bölmesinde, kaydını açmak için bir mobil cihaz markası seçin. Alternatif olarak yeni bir marka oluşturmak için eylem bölmesinde **Yeni**'yi seçin.
1. Yeni veya seçilen cihaz markası kaydının başlık bölümünde, aşağıdaki alanları ayarlayın:

    - **Cihaz markası**: *Microsoft Corporation* gibi cihaz markasının adı.
    - **Açıklama**: Marka adlarını ayırt etmeye yardımcı olacak bir açıklama girebilirsiniz.

1. **Mobil cihaz modelleri** hızlı sekmesi, seçilen cihaz markası için tüm modelleri gösterir. Kılavuza satır eklemek veya satırları kaldırmak için araç çubuğundaki düğmeleri kullanın. Her satır için aşağıdaki alanları ayarlayabilirsiniz:

    - **Cihaz modeli kimliği**: *Surface Book 2* gibi cihaz modeli kimliği.
    - **Açıklama**: Model kimliklerini ayırt etmeye yardımcı olacak bir açıklama girebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

- [Ambar Yönetimi mobil uygulamasını yükleme ve bağlama](install-configure-warehouse-management-app.md)
- [Warehouse Management mobil uygulaması için adım simgeleri ve başlıklar atama](step-icons-titles.md)