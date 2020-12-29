---
title: Regulatory Configuration Service (RCS) - Küreselleşme özellikleri
description: Bu konuda, Küreselleşme özellikleri oluşturmak ve kullanmak için Microsoft Regulatory Configuration Services (RCS) ve Genel depoyu nasıl kullanacağınız açıklanmaktadır.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: ae46dab5250fbe8096f43e420cb7ef33a5862af0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448722"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>Regulatory Configuration Service (RCS) - Küreselleşme özellikleri

[!include [banner](../includes/banner.md)]

Microsoft Regulatory Configuration Service (RCS) kullanarak Globalizasyon hizmetlerinde kullanılabilecek e-faturalama hizmeti gibi bir Globalizasyon özelliği oluşturabilirsiniz. RCS şu görevleri gerçekleştirmenizi sağlar:

- Bir özelliğin ilgili bileşenlerini tanımlayın.
- Özellik yaşam döngüsünü özelliğin durumuyla yönetin.
- Bir özelliği tanımlanmış ortamlar için kullanılabilir hale getirin.
- Bir özelliği diğer organizasyonlarla paylaşma.

Aşağıdaki yordamlarda, RCS 'deki bir kullanıcının Globalizasyon özelliği ve ilgili bileşenleri nasıl ekleneceği, özelliğin durumu nasıl güncelleştirileceği ve genelleştirme hizmetlerinde kullanılabilmesi için özelliğin kullanılabilir hale gelen bir Kullanıcı açıklanmaktadır.

Yordamları gerçekleştirmeden önce, aşağıdaki görevlerle ilgili adımları tamamlamanız gerekir:

- RCS örneğine erişme.
- Bir konfigürasyon sağlayıcısı oluşturma ve etkinleştirme. Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Finance and Operations uygulamaları örneğiniz için aşağıdaki adımları izleyin.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. Şirketiniz için hiçbir RCS ortamı sağlanmamışsa **Regulatory services -Yapılandırma**'yı seçin ve ardından bir ortam sağlamak için yönergeleri izleyin.

> [!NOTE]
> Şirketiniz için zaten bir RCS ortamı sağlanmışsa oturum açma seçeneğini belirleyerek bu ortama erişmek için sayfa URL'sini kullanın.

## <a name="turn-on-the-globalization-features"></a>Globalizasyon özellikleri açma

1. RCS örneğiniz üzerinde **Özellik yönetimi** kutucuğunu seçin.
2. **Özellik Yönetimi** çalışma alanında, listeden **Genelleştirme özellikleri**'ni seçin ve **Şimdi etkinleştir**'i seçin.

    ![Özellik yönetiminde Globalizasyon özellikleri](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>Genelleştirme özellikleri

Genelleştirme özelliğini kullanmak için, onu Global depodan içe aktarmanız ve kendi sürümünüzü oluşturmanız gerekir. Genelleştirme özellikleri eklemenin iki yolu vardır:

- Yayımlanmış veya paylaşılan, varolan bir özelliği temel alan türetilmiş bir özellik ekleyin.
- Sıfırdan oluşturduğunuz yeni bir özellik ekleyin.

## <a name="access-globalization-features"></a>Globalizasyonu özelliklerine erişme

1. Bu konuda daha önce anlatıldığı gibi, özellik yönetiminde **Genelleştirme özellikleri** özelliğinin açık olduğundan emin olun.
2. Yeni **Genelleştirme özellikleri** çalışma alanını açın ve sonra **Özellikler** altında **e-faturalama** döşemesini seçin.

    ![Global Özellikler çalışma alanı](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    **E-faturalama özellikleri** sayfası açılır.

    ![e-faturalama özellikleri sayfası](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>Türetilmiş Genelleştirme özelliği Ekle

Yeni bir Genelleştirme özelliğini, yayımlanmış veya paylaşılan varolan bir özellikten türeterek ekleyebilirsiniz.

1. **Genel havuz sayfasından içe aktarma özelliğini** açmak için **içe aktar**'ı seçin.

    ![Özelliği genel havuz sayfasından içe aktar](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. En son özellikleri almak için **Eşitle** 'yi seçin.

    Eşitlenmiş liste, Microsoft tarafından yayımlandıkları veya başka bir konfigürasyon sağlayıcısı tarafından paylaşıldıklarından dolayı kullanabileceğiniz özellikleri içerir.

    ![Eşitlenen özellik listesi](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. Listede içe aktarılacak özellikleri seçin ve **içe aktar**'ı seçin. Seçilen özellikler başarıyla içe aktarıldığında bir ileti alırsınız.

    ![İleti içe aktarma başarılı](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. **Ekle**'yi seçin ve açılan iletişim kutusunda **varolan sürüme bağlı** seçeneğini belirleyin.
5. Özellik için bir ad ve açıklama girin.
6. Kullanılabilen özellikler listesinde, özelliğin temel sürümünü seçin ve sonra **Özellik Oluştur**'u seçin.

    ![Türetilmiş özellik ekleme](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    Eklediğiniz Özellik oluşturuldu ve **taslak** durumuna sahip.

    ![Taslak durumunda olan türetilmiş Özellik](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. Güncelleştirmelerin gerekli olup olmadığını belirlemek için özellik bileşenlerini gözden geçirin:

    - Elektronik raporlama (ER) biçimlerini ve bunların, özellik sürümü için biçim eşlemeleriyle olan bağlamasını özelleştirmeniz olasılığına karşı konfigürasyonları gözden geçirin.
    - Özellik sürümü için **Eylemler** sekmesini, **uygulanabilirlik kuralları** sekmesini veya **değişkenler** sekmesini özelleştirmeniz gerekebileceği için kurulumu gözden geçirin.

8. **Sürümler** sekmesinde, **geçerlilik başlangıç** tarihi seçin ve **Açıklama** alanı boşsa açıklama girin.
9. Özelliği tamamlamak için **durumu değiştir**'i seçin. Tamamlanmış özellikler belirli bir ortam için kullanılabilir duruma getirilebilir, böylece Genelleştirme hizmetlerinde kullanılabilir veya Global havuzda yayımlanabilir.

> [!NOTE]
> **Yayımlanmış** **özellik sürümü durum** değeri olan Özellikler , harici organizasyonlarla paylaşılabilir.

## <a name="add-a-new-globalization-feature"></a>Yeni Genelleştirme özelliği Ekle

Baştan oluşturarak yeni bir Genelleştirme özelliği ekleyebilirsiniz.

1. **Genel havuzdan içe aktarma özelliği** sayfasında **Ekle** 'yi seçin ve açılan iletişim kutusunda **yeni özellik** seçeneğini belirleyin.
2. Özellik için bir ad ve açıklama girin.
3. **Özellik oluştur**'u seçin.

    ![Yeni özellik ekleme](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. **Sürümler** sekmesinde, **geçerlilik tarihi** seçin ve sonra da özelliği tamamlamak için **durumu değiştir**'i seçin. Tamamlanmış özellikler belirli bir ortam için kullanılabilir duruma getirilebilir, böylece Genelleştirme hizmetlerinde kullanılabilir veya Global havuzda yayımlanabilir.

> [!NOTE]
> **Yayımlanmış** **özellik sürümü durum** değeri olan Özellikler , harici organizasyonlarla paylaşılabilir.

## <a name="feature-component-overview"></a>Özellik bileşenine genel bakış

Genelleştirme özelliklerinin birkaç bileşeni vardır:

- **Sürüm** – Bu bileşen özellik yaşam döngüsü yönetimini destekler ve kullanıcıların özelliğin farklı sürümleri için durumu yönetmesine izin verir.
- **Yapılandırmalar** – Bu bileşen kullanıcıların ilgili ER biçimlerini ve biçim eşlemelerini yönetmesine, görüntülemesine ve düzenlemesine olanak tanır.
- **Ayarlar** – Bu bileşen, bir e-faturalama hizmeti gibi, Genelleştirme servisleri kullanıcılarının ilgili özellik sürümünün kurulumunu yönetme gibi kullanıcılara olanak tanır. Bu nedenle, iletişim ve yanıt kurallarının esnek yapımını destekler.
- **Ortam** – Bu bileşen, bir e-faturalama hizmeti gibi Genelleştirme Hizmetleri kullanıcılarının, özellik sürümü kurulumunun kullanıldığı ortamı yönetmesine ve erişimi olacak kullanıcılara yetki vermesine olanak tanır.
- **Kuruluşlar** – Bu bileşen, kullanıcıların özelliği harici organizasyonlarla paylaşmasına olanak tanır.

## <a name="configuring-feature-components"></a>Özellik bileşenlerini konfigüre etme

### <a name="version-and-status"></a>Sürüm ve durum

Sürüm, Genelleştirme özelliği yaşam döngüsünü yönetmek için kullanılır.

**Durum**, **Sürüm** sekmesinin durum alanında değiştirilebilir  . Aşağıdaki durumlar kullanılabilir:

- **Taslak** – özellik yalnızca bu durumda olduğu zaman düzenlenebilir.
- **Tamamlandı** – özellik ve tüm ilgili bileşenler sonlandırılmalı (tamamlandı) ve düzenlenemez.
- **Yayımlandı** – özellik ve ilgili tüm bileşenler Global depoya yayımlandı.
- **Paylaşılan** – özellik ve tüm ilgili bileşenler harici organizasyonlarla paylaşıldı.
- **Etkin** – özellik ve tüm ilgili bileşenler, bir e-faturalama servisi gibi bir Genelleştirme hizmetinde kullanılmak üzere etkinleştirildi.

> [!NOTE]
> Özelliklerin bazıları bu durumlardan bazıları arasında sırayla hareket etmelidir. Bu nedenle, her yaşam döngüsü aşamasında her durum için kullanılabilir olmayabilir.

### <a name="configurations"></a>Konfigürasyonlar

Yapılandırmalar için şu eylemler mevcuttur:

- **Görüntüle** – herhangi bir güncelleştirme gerektirmeyen temel özellik konfigürasyonlarını görüntüleyin.
- **Düzenle** – Biçim tasarımcısında biçim veya biçim eşleştirmesini düzenleyebilmeniz için seçili konfigürasyonun taslak sürümünü oluşturun.
- **Sil** – Seçili konfigürasyonu özellikten silin.
- **Yeniden temellendirme** – özelliği yeniden temellendir. Daha fazla bilgi için, Bu konunun ilerleyen kısımlarında [türetilen Genelleştirme özellikleri](#rebase) bölümüne bakın.

### <a name="setups"></a>Kurulumlar

Özellik kurulumları için şu eylemler mevcuttur:

- **EKle** – yeni özellik kurulumu oluşturur. Bu özellik Kurulumu varolan bir özellik kurulumundan türetilebilir veya sıfırdan oluşturulabilir.
- **Sil** – Seçili bir özellik kurulumunu siler.
- **Görüntüle** – herhangi bir değişiklik gerektirmeyen temel bir özellik kurulumunu görüntüleyin.
- **Düzenle** – bir özellik kurulumunun üç ana bileşen bileşeni özniteliklerini oluşturur, siler veya değiştirir:

    - Eylemler ve parametreleri
    - Uygulanabilirlik kuralları
    - Değişkenler

![Özellik sürümü kurulum sayfası](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>Ortamlar

Ortamlar için şu eylemler mevcuttur:

- **Etkinleştir** – Seçili bir özellik sürümü için, yayımlanmış bir ortam seçin ve kullanılabilir olması gereken **başlangıç tarihini** seçin. Daha fazla bilgi için, Bu konunun ilerleyen kısımlarında [Etkinleştirme için ortamları yapılandırma](#configureenvironment) bölümüne bakın.
- **İptal** – bir özellik kurulumu için ortamı kaldırır.

### <a name="organizations"></a>Kuruluşlar

Bir Genelleştirme özelliğini harici bir kuruluşla paylaşmak için bu adımları izleyin.

1. **E-faturalama özellikleri** sayfasında, paylaşılacak özelliği ve özellik sürümünü seçin.
2. **Kuruluşlar** sekmesinde **Paylaş**'ı seçin ve açılan iletişim kutusunda kuruluşun etki alanı adını girin.
3. **Paylaş**'ı seçin.

    ![Bir kuruluşla özelliği paylaşma](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

Özellik, seçili kuruluşla paylaşılır ve Genel depodaki bu kuruluş tarafından kullanılabilir. Buradan, özellik kuruluşun RCS örneğine veya Dynamics 365 Finance'e kullanılabilmesi için içe aktarılabilir.

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>Türetilmiş Genelleştirme özelliklerini yeniden temellendirme

Türetilmiş Genelleştirme özelliğini yeni veya güncelleştirilmiş temel özellik sürümüne yeniden temellendirerek oluşturabilirsiniz. Bu şekilde, temel sürümde gerçekleşen değişiklikler otomatik olarak güncelleştirilebilir. Güncelleştirilmiş temel özellik sürümü kaynak konfigürasyon sağlayıcısı tarafından oluşturulur ve daha sonra yayımlanır veya paylaşılıyor.

![Temel özellik sürümü güncelleştirildi](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

Örneğin, oluşturduğunuz bir özelliğin türetilmiş sürümünü yeniden temellendirmek istiyorsanız, önce genel depodan içe aktararak özelliğin en son sürümünü alırsınız.

1. **E-faturalama özellikleri** sayfasında **içe aktar**'ı seçin.
2. En son özellikleri almak için **Eşitle** 'yi seçin.
3. Özellikler listesinde içe aktarılacak özellikleri seçin ve **içe aktar**'ı seçin.

    ![Bir özelliğin en son sürümünü içe aktarma](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. Özellik listesinde, yeniden temellendirme özelliğini seçin.
5. **Sürüm** sekmesinde, taslak sürümünü oluşturmak için **yeni**'yi seçin.

    ![Yeni taslak sürümü oluşturuldu](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. **Yeniden temellendirme** seçin.
7. **Yeniden temellendirme** iletişim kutusunda, tekrar temellendirgitmek için özelliğin en son sürümünü seçin.

    ![Yeniden temellendirme iletişim kutusu](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. **Tamam**'ı seçin.
9. Özellik bileşenlerini gözden geçirin ve gerekli değişiklikleri yapın.
10. Yeniden temellendirilen özelliği tamamlamak için **durumu değiştir**'i seçin. Yeniden temellendirme tamamlandığı zaman ek eylemler gerçekleştirebilirsiniz. Örneğin, özelliği yayımlayabilir ve genelleştirme hizmetlerinde kullanılabilir hale getirebilirsiniz.

    ![Özellik durumu tamamlandı olarak güncelleştirildi](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>Genelleştirme özellikleri için ortamları konfigüre etme

Genelleştirme hizmetlerinin kullanıcıları, bir Genelleştirme özelliği ayarlamak ve erişim izni olacak diğer kullanıcılara yetki vermek için ortamı yönetebilir.

1. **Genelleştirme özellikleri** çalışma alanında ve sonra **Ortamlar** altında **e-faturalama** döşemesini seçin.

    ![Globalizasyon Özellikler çalışma alanı](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. **Anahtar kasa parametrelerini** seçin ve sonra bir Azure anahtar kasa parolası oluşturmak için **yeni** 'yi seçin.
3. Anahtar Kasası için bir ad ve açıklama girin ve sonra **anahtar kasa URI** alanına Azure 'Da anahtar kasa kaynağını tanımlayan URL 'yi girin.
4. **Sertifikalar** hızlı sekmesinde, sertifikayı eklemek için **Ekle**'yi seçin ve her bir sertifika için bir ad ve açıklama girin.

    ![Sertifika eklendi](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. Yeni bir ortam oluşturmak için **Yeni**'yi seçin.
6. Depolama için gereken bir ad, açıklama ve paylaşılan erişim imza belirteci gizli girin.
7. Bu ortama erişim izni olacak kullanıcıyı eklemek için, **kullanıcılar** hızlı sekmesinde, **yeni**'yi seçin.
8. Kullanıcının Kullanıcı kodunu ve e-posta adresini girin.
9. Daha fazla kullanıcı eklemek için 7 - 8 arasındaki adımları tekrarlayın.
10. Ortamı yayımlamak için **Yayımla**'yı seçin.

    ![Yayımlanan ortam](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)
