---
title: Üretim katı yürütme arabiriminde tatil bakiyelerini görüntüle
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'in çalışanlara cari yıl için tatil bakiyelerine genel bir bakış sağlamak üzere bordro istatistiklerini kullanacak şekilde nasıl ayarlanacağını gösteren örnek bir senaryo sağlanmaktadır.
author: johanhoffmann
ms.date: 04/22/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.XX
ms.openlocfilehash: a97858c72b0be50609cee552bd0635e2d68ea478
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645365"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>Üretim katı yürütme arabiriminde tatil bakiyelerini görüntüle

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'in her bir çalışana cari yıl için tatil bakiyelerine genel bir bakış sağlamak üzere bordro istatistiklerini kullanacak şekilde nasıl ayarlanacağını gösteren örnek bir senaryo sağlanmaktadır. Çalışanlar, tatil bakiyelerini üretim katı yürütme arabirimindeki **Günüm** iletişim kutusunda görebilir.

Bu senaryoda, tatil yılının 1 Eylül'den 31 Ağustos'a kadar sürdüğü Danimarka tatil yasası kullanılır. Bu senaryoda, şirketiniz yeni bir çalışan işe aldı ve bu çalışana geçerli tatil yılının geri kalanı için 10 tatil günü bakiyesi verecek.

## <a name="turn-on-the-required-features"></a>Gerekli özellikleri açma

Bu senaryoyu çalıştırmak için, [Özellik yönetimindeki](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) *Üretim katı yürütme arabirimi özelliği için "Günüm" görünümünü* etkinleştirmeniz gerekir. Üretim katı yürütme arabirimi için bu ve diğer özelliklerin nasıl etkinleştirileceği hakkında bilgi için bkz. [Üretim katı yürütme arabirimini yapılandırma](production-floor-execution-configure.md).

## <a name="make-sample-data-available"></a>Örnek verilerini kullanılabilir hale getirme

Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

## <a name="create-a-new-pay-type"></a>Yeni bir ödeme türü oluştur

İşçilerin kazandıkları tatil günlerini (*tatil bakiyeleri* olarak da adlandırılır) izleyecek yeni bir *ödeme türü* oluşturarak başlayın. Tipik olarak, ücret türleri işçilerin ücretini hesaplamak için kullanılır. Ancak, burada oluşturduğunuz ödeme türü bakiyeyi hesaplamak için kullanılır.

1. **Saat ve işe devam \> Kurulum \> Bordro \> Ödeme türleri**'ne gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Ödeme türü:** *5151-1*
    - **Açıklama:** *Çalışan tatil günleri için sayaç*
    - **Dışa aktarmaya dahil et:** *Hayır*

## <a name="update-the-pay-agreement"></a>Ödeme sözleşmeyi güncelleştir

Bu bölümde, yeni ödeme türünü ekleyerek ve tatil günleri kaydedildiğinde her çalışanın tatil bakiyesinin nasıl ayarlanacağını tanımlayan kuralları ayarlayarak mevcut bir *ödeme sözleşmesini* düzenleyeceksiniz.

1. **Saat ve işe devam \> Kurulum \> Bordro \> Ödeme anlaşmaları**'na gidin.
1. Tatil ilkesini ayarlamak istediğiniz ödeme sözleşmesini seçin. (Standart USMF örnek verileriyle çalışıyorsanız yalnızca bir ödeme sözleşmesi vardır, *Man*.)
1. Seçilen ödeme sözleşmesinin geçerli tarih için geçerli olduğundan emin olun. Standart USMF örnek verileriyle çalışıyorsanız *Man* ödeme sözleşmesinin **Bitiş tarihi** alanı geçmişteki bir tarihe ayarlanmış olabilir. Değeri, gerektiğinde gelecekte bir veya iki yıl olacak şekilde değiştirin.
1. Eylem Bölmesinde, **Sözleşme satırları**'nı seçin.
1. **Ödeme sözleşmesi satırları** sayfasında, **Genel Bakış** Hızlı Sekmesinde, araç çubuğunda aşağıdaki değerleri ayarlayın:

    - İlk açılır listeden **Pazartesi**'yi seçin.
    - İkinci açılır listeden **Devamsızlık**'ı seçin.

1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda, **Ödeme türü** alanını bu senaryo için oluşturduğunuz ödeme tipine ayarlayın ( *5151-1*). Diğer tüm alanları, varsayılan değerleriyle bırakın.
1. Yeni satır seçiliyken, **Genel** hızlı sekmesinde aşağıdaki değerleri ayarlayın:

    - **Devamsızlık kodu:** *Tatil*
    - **Sabit miktarı kullan:** *Evet*
    - **Sabit:** *-1*

1. Eylem Bölmesi'nde, **Günü kopyala**'yı seçin.
1. **Günü kopyala** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Salı**, **Çarşamba**, **Perşembe** ve **Cuma:** *Evet*
    - **Üzerine yaz:** *Evet*
    - **Devamsızlık:** *Evet*

1. **Tamam**'ı seçin.

## <a name="create-a-payroll-statistic-group"></a>Bir bordro istatistiği grubu oluşturma

*Bordro istatistik grupları*, bir dönem boyunca çalışan kayıtları için istatistik ayarlamak amacıyla kullanılır. Bu senaryoda, çalışanların bir tatil döneminde kazanmakta olduğu tatil günlerinin sayısını hesaplamak için bir bordro istatistik grubu kullanacaksınız. Danimarka'da, tatil dönemi 1 Eylül ile 31 Ağustos arasında çalışır.

1. **Saat ve işe devam \> Kurulum \> Bordro \> Bordo istatistik grupları**'na gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Bordro istatistik grubu:** *VAC*
    - **Açıklama:** *Tatil bakiyesi*
    - **Transfer:** *Hayır*

1. Yeni satır seçiliyken, Eylem Bölmesinde **Kurulum**'u seçin.
1. Eylem Bölmesinde, **Kurulum** sayfasında ızgaraya satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda, **Ödeme türü** alanını *5151-1* olarak ayarlayın.
1. **Dönem kodu** alanını seçin ve basılı tutun (veya sağ tıklayın) ve sonra **Ayrıntıları görüntüle**'yi seçin. Artık, bu alana daha sonra atayacağınız dönem kodunu ayarlayabilirsiniz.
1. **Dönem türleri** sayfasında, Eylem Bölmesi'nde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Dönem türleri:** *VacYear*
    - **Açıklama:** *Tatil yılı*
    - **Sıklık:** *Yıl*

1. Yeni satır seçiliyken, Eylem Bölmesinde **Dönem oluştur**'u seçin.
1. **Dönem oluştur** iletişim kutusunda aşağıdaki değerleri ayarlayın.

    - **Dönemin başlangıç tarihini belirtin:** *1 Eylül 2021*
    - **Dönem uzunluğu:** *5*

1. **Tamam**'ı seçin.
1. **Bordro istatistik grupları** sayfasına dönmek için **Dönem türleri** sayfasını kapatın.
1. **Dönem kodu** alanını henüz oluşturduğunuz dönem türü olarak ayarlayın (*VacYear*).

## <a name="create-a-statistical-balance-setup"></a>İstatistiksel bakiye kurulumu oluşturun

Bu bölümde, önceki bölümde oluşturduğunuz bordro istatistik grubuyla bağlantılı *istatistiksel bir bakiye kurulumu* oluşturacaksınız. Daha sonra, bu istatistiksel bakiye kurulumunu üretim emri arabirimindeki **Günüm** görünümüne bağlayacaktır. **Günüm** görünümü böylece, ilişkili bordro istatistik grubuna atanmış ödeme türü için tatil bakiyelerini gösterebilir.

1. **Saat ve işe devam \> Kurulum \> Bordro \> İstatistik bakiye kurulumu**'na gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Bordro istatistik grubu:** *VAC*
    - **Harici ad:** *Tatil bakiyesi*
    - **Esnek:** *Hayır*

## <a name="create-a-manual-premium"></a>El ile belirlenen prim oluşturma

*El ile prim*, genellikle ek çalışma için çalışanlara fazladan ödeme vermek amacıyla kullanılır. Bu senaryoda, her çalışanın ilk tatil bakiyesini ayarlamak için kullanabileceğiniz bir el ile prim oluşturacaksınız.

1. **Saat ve işe devam \> Kurulum \> Bordro \> El ile prim**'e gidin.
1. Eylem Bölmesi'nde, bir kayıt eklemek için **Yeni**'yi seçin.
1. Yeni kayıtta aşağıdaki değerleri ayarlayın:

    - **Primler:** *VAC*
    - **Açıklama:** *Çalışanların tatil bakiyesini ayarlama*
    - **Ödeme türü:** *5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>Çalışanın ilk tatil bakiyesini ayarla ve bu günü bir gün olarak ayarla

Bordro yöneticileri çalışanların günlük kayıtlarını gözden geçirip onaylamamak için **Onayla** sayfasını kullanırlar. Bu senaryoda, bir alt işin başlangıç tatil bakiyesini ayarlayabilmek ve çalışanın gerçekleştirdiği tatil günlerini kaydetmek için bir yönetici rolü yanınızda olur.

1. **Zaman ve işe devam \> Gözden geçirme ve onaylama \> Onaylama**'ya gidin.
1. **Onaylama** iletişim kutusunda aşağıdaki alanları ayarlayın:

    - **Onay grubu** – Ait olduğunuz onay grubunu seçin. (Standart USMF örnek verileriyle çalışıyorsanız yalnızca bir onay grubu vardır, *AdmMan*.)
    - **Tüm grubu görüntüle, 1 gün** – Seçeneği belirleyin ve sonra alanı geçerli tarih olarak ayarlayın.

1. **Tamam**'ı seçin.
1. **Onaylama** sayfası ölçütünüze uyan kayıtların listesini gösterir. Onaylamak istediğiniz çalışanı seçin. Standart USMF örnek verileriyle çalışıyorsanız, çalışan *000496*'yı ( *Christina Portra*) seçin.
1. Seçili çalışana 10 günlük tatil izni ver:

    1. Çalışan seçiliyken, Eylem Bölmesinde **Prim satırları**'nı seçin.
    1. **Prim satırları** sayfasında, Eylem Bölmesi'nde, kılavuza satır eklemek için **Yeni**'yi seçin.
    1. Yeni satırda aşağıdaki değerleri ayarlayın:

        - **Primler:** *VAC*
        - **Miktar:** *10*

    1. **Prim satırları** sayfasını kapatın.

1. **Onaylama** sayfasında, çalışanın, tatil günlerinden birini geçerli tarihte kullandığı gerçeği kaydedin:

    1. Çalışan hâlâ seçiliyken, ızgaraya satır eklemek için, sayfanın alt kısmındaki **Genel bakış** sekmesinde araç çubuğundan **Yeni**'yi seçin.
    1. Yeni satırda aşağıdaki değerleri ayarlayın:

        - **Günlük kayıt türü:** *Devamsızlık*
        - **Referans:** *Tatil*

    1. Tatil bakiyesini uygulamak ve indirimi hesaplamak için, sayfanın üst kısmında, araç çubuğundan **Transfer**'i seçin.

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>Üretim tabanı yürütme arabirimini, Günüm iletişim kutusunu içerecek şekilde konfigüre edin

Bu bölümde, üretim tabanı yürütme arabirimine **Günüm** düğmesi ekleyeceksiniz. Böylece çalışanlar bu düğmeyi, **Günüm** iletişim kutusunu açmak için kullanabilir.

1. **Üretim denetimi \> Ayarlar \> Üretim yürütme \> Üretim katı yürütmesini konfigüre et**'e gidin.
1. *Varsayılan* gibi bir yapılandırma seçin.
1. Eylem Bölmesinde, **Sekme tasarla**'yı seçin.
1. Bu sekme ayarlarını görmek için, liste bölmesinde, **Tasarım sekmeleri** sayfasında, *Tüm işler*'i seçin. **Ana görünüm** alanı şimdi *Tüm işlerin* değerini göstermelidir.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **İkincil araç çubuğu** hızlı sekmesinde, **Kullanılabilir eylemler** sütununda, **Günüm**'ü seçin. Ardından, bunu **Seçili eylemler** sütununa taşımak için sağ ok düğmesini seçin.

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>Üretim katı yürütme arabiriminde bakiyenizi kontrol edin

Bu bölümde, en son tatil süresini daha önce ayarladığınız çalışan olarak üretim tabanı yürütme arabiriminde oturum açacaksınız. Böylece, tatil bakiyenizi görüntülemek için **Günüm** iletişim kutusunu açarsınız.

1. **Üretim denetimi \> Kurulum \> Üretim yürütme \> Üretim katı yürütmesi**'ne gidin.
1. Bir konfigürasyon seçmeniz istenirse, bu senaryoda daha önce ayarladığınız konfigürasyonu seçin ( *Varsayılan*).
1. Bu senaryoda daha önce ayarladığınız kullanıcı olarak oturum açın. Standart USMF örnek verileriyle çalışıyorsanız, **Rozet Kodu** alanına *123* girerek oturum açabilirsiniz. Bu rozet kodu, Christina Portra'ya karşılık gelir.
1. Sol araç çubuğundan **Günüm**'ü seçin.
1. İletişim kutusunun **Bakiyeler** kısmını denetleyin. Bu bölüm, şimdi dokuz tatil gününe sahip olduğunuz bir bakiye göstermelidir.
