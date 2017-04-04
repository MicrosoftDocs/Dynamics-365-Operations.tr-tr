---
title: Elektronik raporlama hedefleri
description: "Her bir Elektronik raporlama (ER) biçimi yapılandırması ve bunun çıkış bileşeni (bir klasör veya bir dosya) için bir hedef yapılandırabilirsiniz. Uygun erişim hakları verilmiş kullanıcılar çalışma zamanında hedef ayarlarını da değiştirebilir. Bu makalede, ER hedef yönetimi, desteklenen hedeflerin türleri ve güvenlik ile ilgili hususlar açıklanır."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: d38d05fe445bf0326d408038dff84ccf8c0ff64c
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-destinations"></a>Elektronik raporlama hedefleri

Her bir Elektronik raporlama (ER) biçimi yapılandırması ve bunun çıkış bileşeni (bir klasör veya bir dosya) için bir hedef yapılandırabilirsiniz. Uygun erişim hakları verilmiş kullanıcılar çalışma zamanında hedef ayarlarını da değiştirebilir. Bu makalede, ER hedef yönetimi, desteklenen hedeflerin türleri ve güvenlik ile ilgili hususlar açıklanır.

Elektronik raporlama (ER) biçim yapılandırmaları genellikle en az bir çıkış bileşeni içerir: dosya. Genelde yapılandırmalar tek veya birden fazla klasörde gruplanan farklı türlerde birden fazla dosya çıkış bileşeni içerir (örneğin, XML, TXT veya XLSX). ER hedef yönetimi her bir bileşen çalıştırıldığında ne olduğunu önceden yapılandırmanızı sağlar. Bir yapılandırma çalıştırdığınızda, varsayılan olarak, kullanıcı bir dosyayı kaydetmeye veya açmaya olanak tanıyan bir iletişim kutusu görüntülenir. Aynı çalışma biçimi bir ER yapılandırmasını içe aktardığınızda ve bunun için belli bir hedef yapılandırmadığınızda da kullanılır. Ana çıkış bileşeni için bir hedef oluşturulduktan sonra bu hedef varsayılan davranışı geçersiz kılar ve klasör veya dosya hedef ayarlarına göre gönderilir.

## <a name="availability-and-general-prerequisites"></a>Kullanılabilirlik ve genel önkoşulları
ER hedefler işlevselliği Microsoft Dynamics 365 işlemleri 7.0 (Şubat 2016) sürümü için kullanılamaz. Bu nedenle, bu konuda açıklanan tüm işlevleri kullanmak (Kasım 2016 sürüm) işlemleri için Microsoft Dynamics 365 yüklemeniz gerekir. Alternatif olarak, aşağıdaki önkoşulların bir tanesi de yükleyebilirsiniz. Ancak, bu seçenek daha sınırlı bir ER hedef deneyimi sağlar unutmayın.

-   Microsoft Dynamics 365 işlemleri uygulama sürümünün 7.0.1 (Mayıs 2016)
-   ER hedef yönetimi [uygulama düzeltmesi](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Yalnızca içe aktarılan ER yapılandırmaları ve **Elektronik raporlama yapılandırmaları** sayfasında kullanılabilen biçimler için hedefleri ayarlayabilirsiniz.

## <a name="overview"></a>Genel Bakış
ER hedef yönetim işlevleri kullanılabilir **kuruluş yönetim**&gt;**elektronik raporlama**. Burada, bir yapılandırma için varsayılan davranışı geçersiz kılabilirsiniz. **Yeni** ve sonra **Referans** alanına tıklayıncaya kadar içe aktarılan yapılandırmalar gösterilmez, hedef ayarlarını oluşturmak için bir yapılandırma seçin.

[![Bir yapılandırma başvuru alanı seçme](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Başvuru oluşturduktan sonra her klasör veya dosya için bir dosya hedef oluşturabilirsiniz. 

[![Bir hedef dosyasını oluşturma](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Not:** Klasör veya dosya gibi **Dosya Adı** alanında seçilen aynı biçimdeki her bir çıkış bileşeni için bir dosya hedefi oluşturabilirsiniz. Etkinleştirme ve devre dışı bırakmak için hedef dosyasını tek tek hedefleri **hedef ayarları** iletişim kutusu. **Ayarlar** düğmesi seçili dosya hedefi için tüm hedefleri denetlemek amacıyla kullanılır. **Hedef ayarları** iletişim kutusunda **Etkin** seçeneğini ayarlayarak her hedefi ayrı olarak denetleyebilirsiniz.

[![Hedef Ayarları iletişim kutusu](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Hedef türleri
Çeşitli hedef türleri desteklenir. Tüm türleri aynı anda devre dışı bırakabilir veya etkinleştirebilirsiniz. Bu şekilde hiçbir işlem yapmayabilir veya bileşeni tüm yapılandırılmış hedeflere gönderebilirsiniz. Desteklenen hedefler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="email-destination"></a>E-posta hedefi

E-posta ile bir çıkış dosyası göndermek için **Etkin **değerini **Evet** olarak ayarlayın. Bu seçenek etkinleştirildikten sonra e-posta alıcıları belirtin ve konu ve e-posta iletisinin gövdesinde düzenleyin. Sabit e-posta konu ve gövde metinleri ayarlayabilirsiniz veya ER formülleri dinamik olarak e-posta metinleri oluşturmak için kullanabilirsiniz. E-posta adresleri için ER iki şekilde yapılandırabilirsiniz. Yapılandırma işlemleri için Dynamics 365 için yazdırma yönetimi özelliği tamamlandıktan aynı yolla tamamlanabilir. Alternatif olarak, doğrudan bir başvuru ER yapılandırması aracılığıyla bir formül kullanarak bir e-posta adresini çözebilir.

### <a name="email-address-types"></a>E-posta adresi türleri

Tıklattığınızda **düzenleme** için **için** veya **bilgi** alan **için e-posta** iletişim kutusu görüntülenir. Daha sonra kullanmak üzere e-posta adresi türünü seçebilirsiniz.

[![İletişim kutusuna e-posta](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Yazdırma yönetimi

Seçerseniz **yazdırma yönetimi e-posta** türü, sabit bir e-posta adreslerini girebilirsiniz **için** alan. Sabit olmayan e-posta adresi kullanmak için bir dosya hedef için e-posta kaynak türünü seçmeniz gerekir. Aşağıdaki değerleri desteklenir: **müşteri**, **satıcı**, **aday**, **kişi**, **rakip**, **alt**, **başvuran**, **muhtemel satıcı**, ve **izin verilmeyen satıcı**. Bir e-posta kaynak türünü seçtikten sonra düğme yanında kullanmak **kaynak hesabın e-posta** alan açmak için ** formül tasarımcısı ** formu. Parti seçili hesap için e-posta hedef gösteren bir formül eklemek için bu formu kullanabilirsiniz.

[![Yazdırma Yönetimi e-posta türü yapılandırma](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Formüllerin ER yapılandırmasına özgü olduğunu unutmayın. **Formül** alanında bir müşteri veya satıcı tarafı türü için belgeye özgü bir referans girin. Yazmak yerine, müşteri veya satıcı hesabını temsil eden bir veri kaynağı düğümünü bulabilir ve sonra formülü güncelleştirmek için **Veri kaynağı ekle** 'ye tıklayabilirsiniz. Örneğin, ISO 20022 Borç Transferi yapılandırmasını kullanıyorsanız bir satıcı hesabını temsil eden düğüm **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** olur. Aksi takdirde, bir formül kaydetmek için **DE-001** gibi herhangi bir dize değeri girin.

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

İçinde **için e-posta** iletişim kutusunda, geri dönüşüm kutusu sonrakine tıklatın **kaynak hesabın e-posta** e-posta kaynak hesabı için formülü kalıcı olarak silmek için alan. Alternatif olarak, önceden kaydedilmiş bir formülü değiştirmek için formül tasarımcısını açın. E-posta adresleri atamak için tıklatın **düzenleme** açmak için **e-posta adresleri ata** iletişim kutusu.

[![E-posta adresleri için bir e-posta hedef atama](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigürasyon e-postası

Kullandığınız yapılandırma veri kaynaklarında bir e-posta adresini gösteren bir düğüm varsa, bu e-posta türü kullanın. Doğru biçimlendirilmiş bir e-posta adresini almak için formül tasarımcıda veri kaynakları ve işlevlerini kullanabilirsiniz.

[![Bir e-posta adresi veri kaynağı için bir e-posta hedef atama](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Not:** Basit Posta Aktarım Protokolü (SMTP) sunucusu yapılandırılmalı ve kullanılmalıdır. At Dynamics 365 işlemleri için SMTP sunucunuza belirtebilirsiniz **Sistem Yönetimi**&gt;**Kurulum**&gt;**e-posta**&gt;**e-posta parametreleri**.

### <a name="archive-destination"></a>Arşiv hedefi

Microsoft SharePoint klasörü veya Microsoft Azure Depolamaya çıktı göndermek için bu seçeneği kullanabilirsiniz. Seçili belge türü ile tanımlanan bir hedefe çıktı göndermek için **Etkin** değerini **Evet **olarak ayarlayın. Yalnızca grubun **Dosya** olarak ayarlandığı belge türleri seçim için kullanılabilir. Belge türlerini tanımlamak **kuruluş yönetim**&gt;**belge yönetimi**&gt;**belge türleri**. ER hedefleri için yapılandırma, belge yönetim sistemi için yapılandırma ile aynıdır.

[![Belge türleri sayfası](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Konum dosyanın kaydedildiği yeri belirler. Sonra **arşiv** hedef etkinleştirilmişse, iş arşivde yapılandırma Yürütme sonuçlarını kaydedilebilir. Sonuçları görüntüleyebilirsiniz **kuruluş yönetim**&gt;**elektronik raporlama**&gt;**elektronik raporlama arşivlenmiş işleri**. **Not:** adresindeki işlemleri için Dynamics 365 proje arşiv için bir belge türü seçin **kuruluş yönetim**&gt;**çalışma**&gt;**elektronik raporlama**&gt;**parametrelerini bildirdiği elektronik**.

#### <a name="sharepoint"></a>SharePoint

Dosyayı belirlenen bir SharePoint klasörüne kaydedebilirsiniz. Varsayılan SharePoint sunucusunda tanımladığınız **kuruluş yönetim**&gt;**belge yönetimi**&gt;**belge yönetim parametreleri**, **SharePoint** sekme. SharePoint klasörü yapılandırdıktan sonra belge türü için ER Çıktının kaydedileceği klasörü olarak seçebilirsiniz. 

[![Bir SharePoint klasörünü seçme](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure Depolama

Belge türü **Arşiv dizini** olarak ayarlandığında bir dosyayı Azure Depolama'ya kaydedebilirsiniz.

### <a name="file-destination"></a>Dosya hedefi

Ayarlarsanız **etkin** için **Evet**, bir yapılandırma çalışmasını bitirdikten sonra Aç veya Farklı Kaydet iletişim kutusu görüntülenir.

### <a name="screen-destination"></a>Ekran hedef

Ayarlarsanız **etkin** için **Evet**, çıktının bir önizleme oluşturulur. XML, TXT veya PDF gibi bazı dosya türlerini doğrudan bir tarayıcı penceresinde görüntüleyebilirsiniz. Diğer dosya türleri için böyle bir Microsoft Excel veya Word, Microsoft Office Online hizmeti kullanılır.

### <a name="power-bi-destination"></a>Güç BI hedef

Set **etkin** için **Evet** ER yapılandırmanızı örneğiniz Dynamics 365 gelen veri aktarımını işlemlerinde Microsoft Power BI hizmetlerini düzenlemek için kullanılacak. Aktarılan dosyalar bu amaç için yapılandırılmış bir Microsoft SharePoint Server örneği üzerinde depolanır. Daha fazla bilgi için bkz: [güç BI verilerle Dynamics 365 işlemleri için sağlamak için bir elektronik raporlama yapılandırmasını kullanın](general-electronic-reporting-report-configuration-get-data-powerbi.md). **İpucu:** Varsayılan davranışı geçersiz kılmak amacıyla (bir yapılandırma için iletişim kutusu) ana çıkış bileşeni için bir hedef referansı ve bir dosya hedefi oluşturabilir ve sonra tüm hedefleri devre dışı bırakabilirsiniz.

## <a name="security-considerations"></a>Güvenlik ile ilgili hususlar
ER hedefleri için iki tür ayrıcalık ve görev kullanılır. Bir tür denetleyen tüzel kişilik için yapılandırılmış olan genel hedeflere koruma becerisi (diğer bir deyişle, erişimi kontrol eder **hedefleri bildirdiği elektronik** sayfa). Diğer tür çalışma zamanında bir uygulama kullanıcısının ER geliştirici veya ER işlev danışmanı ile yapılandırılan hedef ayarlarını geçersiz kılma yeteneğini denetler.

| Rol (AOT adı)                     | Rol adı                                  | Görev (AOT adı)                     | Görev adı                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Elektronik raporlama geliştirici             | ERFormatDestinationConfigure        | Elektronik raporlama biçimi hedefini yapılandır                |
| ERFunctionalConsultant              | Elektronik raporlama işlev danışmanı | ERFormatDestinationConfigure        | Elektronik raporlama biçimi hedefini yapılandır                |
| PaymAccountsPayablePaymentsClerk    | Borç hesapları ödeme memuru            | ERFormatDestinationRuntimeConfigure | Çalışma zamanında kullanılacak elektronik raporlama biçimi hedefini yapılandır |
| PaymAccountsReceivablePaymentsClerk | Alacak hesapları ödeme memuru         | ERFormatDestinationRuntimeConfigure | Çalışma zamanında kullanılacak elektronik raporlama biçimi hedefini yapılandır |

**Not:** Önceki görevlerde iki ayrıcalık kullanılır. Bu ayrıcalıklar ilgili görevlerle aynı adlara sahiptir: **ERFormatDestinationConfigure** ve **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Sıkça sorulan sorular
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Elektronik yapılandırmaları içe aktardım ve bunları Elektronik raporlama yapılandırmaları sayfasında görüyorum. Ama neden bunları elektronik raporlama destinations sayfasında görmüyorum?

Tıklattığınızdan emin olun **yeni** ve sonra bir yapılandırma seçin **başvuru** alan. **Elektronik raporlama hedefleri** sayfasında yalnızca hedeflerin yapılandırıldığı yapılandırmaları görebilirsiniz.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Hangi hesap Azure depolama ve Azure Blob Depolama Birimi kullanılan tanımlamak için bir yol var mı?

Hayır. Tanımlanan ve belge yönetim sistemi için kullanılan varsayılan Azure Blob Depolama Birimi kullanılır.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Hedef ayarları dosyasını hedef amacı nedir? Bu ayar ne işe yarar?

**Dosya** hedefi bir iletişim kutusunu denetlemek için kullanılır. Bu hedef etkinleştirin ya da herhangi bir hedef için bir konfigürasyon olarak tanımlanmışsa, açık bir bakın veya çıktı dosyası oluşturulduktan sonra Kaydet iletişim kutusu.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>E-posta gönderebileceğim bir satıcı hesabını referans gösteren bir formül örneği verebilir misiniz?

Formül ER yapılandırmasına özgüdür. Örneğin, ISO 20022 Borç Transferi yapılandırmasını kullanırsanız ilgili satıcı hesabını almak için **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** veya **model.Payments.Creditor.Identification.SourceID** 'yi kullanabilirsiniz.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Biçim yapılandırmalarımdan biri bir klasörde gruplandırılmış birden fazla dosya içeriyor (örneğin, Klasör1 Dosya1, Dosya2 ve Dosya3'ü içeriyor). Klasör1.zip klasörünün hiçbir zaman oluşmaması, Dosya1'in e-posta ile gönderilmesi, Dosya2'nin SharePoint'e gönderilmesi ve yapılandırma çalışır çalışmaz Dosya3'ü açabilmem için hedefleri nasıl ayarlarım?

Biçiminiz ER yapılandırmalarda kullanılabilir önkoşuldur. Kendi biçiminiz varsa **Elektronik raporlama hedefi** sayfasını açın ve bu yapılandırma için yeni bir referans oluşturun. Sonra her bir çıkış bileşeni için bir adet olmak üzere dört dosya hedefinizin olması gerekir. İlk dosya hedefini oluşturun, buna **Klasör** gibi bir ad verin ve yapılandırmanızda klasörü gösteren bir dosya adı seçin. Sonra **Ayarlar**'a tıklayın ve tüm hedeflerin devre dışı bırakıldığından emin olun. Bu dosya hedefi için klasör oluşturulmayacaktır. Varsayılan olarak, dosyalar ve ana klasörler arasındaki hiyerarşik bağımlılıklar nedeniyle dosyalar aynı şekilde davranmayacaktır. Diğer bir deyişle, bunlar her yere gönderilemeyecektir. Bu varsayılan davranışı geçersiz kılmak için her bir dosya için bir adet olmak üzere üç dosya daha oluşturmanız gerekir. Her biri için hedef ayarlarında dosyanın gönderilmesi gereken hedefi etkinleştirmeniz gerekir.

# <a name="see-also"></a>Ayrıca bkz.

[Elektronik raporlamaya genel bakış](general-electronic-reporting.md)


