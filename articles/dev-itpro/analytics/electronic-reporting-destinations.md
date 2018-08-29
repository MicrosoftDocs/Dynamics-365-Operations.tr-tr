---
title: Elektronik raporlama (ER) hedefleri
description: "Her bir Elektronik raporlama (ER) biçimi yapılandırması ve bunun çıkış bileşeni (bir klasör veya bir dosya) için bir hedef yapılandırabilirsiniz. Uygun erişim hakları verilmiş kullanıcılar çalışma zamanında hedef ayarlarını da değiştirebilir. Bu makalede, ER hedef yönetimi, desteklenen hedeflerin türleri ve güvenlik ile ilgili hususlar açıklanır."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 3aa27b3ac263c6c952de7e4b508f48f21ba489ad
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="electronic-reporting-er-destinations"></a>Elektronik raporlama (ER) hedefleri

[!include [banner](../includes/banner.md)]

Her bir Elektronik raporlama (ER) biçimi yapılandırması ve bunun çıkış bileşeni (bir klasör veya bir dosya) için bir hedef yapılandırabilirsiniz. Uygun erişim hakları verilmiş kullanıcılar çalışma zamanında hedef ayarlarını da değiştirebilir. Bu makalede, ER hedef yönetimi, desteklenen hedeflerin türleri ve güvenlik ile ilgili hususlar açıklanır.

Elektronik raporlama (ER) biçim yapılandırmaları genellikle en az bir çıkış bileşeni içerir: dosya. Genelde yapılandırmalar tek veya birden fazla klasörde gruplanan farklı türlerde birden fazla dosya çıkış bileşeni içerir (örneğin, XML, TXT veya XLSX). ER hedef yönetimi her bir bileşen çalıştırıldığında ne olduğunu önceden yapılandırmanızı sağlar. Bir yapılandırma çalıştırıldığında, varsayılan olarak, kullanıcının bir dosyayı açmasına veya kaydetmesine izin veren bir iletişim kutusu gösterilir. Aynı çalışma biçimi bir ER yapılandırmasını içe aktardığınızda ve bunun için belli bir hedef yapılandırmadığınızda da kullanılır. Ana çıkış bileşeni için bir hedef oluşturulduktan sonra bu hedef varsayılan davranışı geçersiz kılar ve klasör veya dosya hedef ayarlarına göre gönderilir.

## <a name="availability-and-general-prerequisites"></a>Kullanılabilirlik ve genel önkoşulları
ER hedeflerinin işlevselliği Microsoft Dynamics AX 7.0 (Şubat 2016) sürümünde kullanılamaz. Bu nedenle, bu konuda açıklanan tüm işlevleri kullanabilmek için Microsoft Dynamics 365 for Operations sürüm 1611'i (Kasım 2016) yüklemeniz gerekir. Alternatif olarak, aşağıdaki önkoşullardan birini de yükleyebilirsiniz. Ancak, bu alternatifin daha sınırlı bir ER hedef deneyimi sağladığını unutmayın.

-   Microsoft Dynamics AX uygulama sürümü 7.0.1 (Mayıs 2016)
-   ER hedef yönetimi [uygulama düzeltmesi](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Yalnızca içe aktarılan ER yapılandırmaları ve **Elektronik raporlama yapılandırmaları** sayfasında kullanılabilen biçimler için hedefleri ayarlayabilirsiniz.

## <a name="overview"></a>Genel Bakış
ER hedef yönetimi işlevselliği, **Organizasyon yönetimi** &gt; **Elektronik raporlama**'da kullanılabilir. Burada, bir yapılandırma için varsayılan davranışı geçersiz kılabilirsiniz. **Yeni** ve sonra **Referans** alanına tıklayıncaya kadar içe aktarılan yapılandırmalar gösterilmez, hedef ayarlarını oluşturmak için bir yapılandırma seçin.

[![Referans alanında bir yapılandırma seçmek](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Referans oluşturduktan sonra her klasör veya dosya için bir dosya hedefi oluşturabilirsiniz. 

[![Bir dosya hedefi oluşturma](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

> [!NOTE] 
> Klasör veya dosya gibi **Dosya Adı** alanında seçilen aynı biçimdeki her bir çıkış bileşeni için bir dosya hedefi oluşturabilirsiniz. Sonra dosya için tekil hedefleri **Hedef ayarları** iletişim kutusunda etkinleştirebilir ve devre dışı bırakabilirsiniz. **Ayarlar** düğmesi seçili dosya hedefi için tüm hedefleri denetlemek amacıyla kullanılır. **Hedef ayarları** iletişim kutusunda **Etkin** seçeneğini ayarlayarak her hedefi ayrı olarak denetleyebilirsiniz.

[![Hedef ayarları iletişim kutusu](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Hedef türleri
Çeşitli hedef türleri desteklenir. Tüm türleri aynı anda devre dışı bırakabilir veya etkinleştirebilirsiniz. Bu şekilde hiçbir işlem yapmayabilir veya bileşeni tüm yapılandırılmış hedeflere gönderebilirsiniz. Desteklenen hedefler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="email-destination"></a>E-posta hedefi

E-posta ile bir çıkış dosyası göndermek için **Etkin** değerini **Evet** olarak ayarlayın. Bu seçenek etkinleştirildikten sonra e-posta konusunu ve metnini düzenleyebilir ve e-posta alıcılarını belirtebilirsiniz. E-posta metni ve konusu için sabit metinler ayarlayabilir veya ER formüllerini kullanarak dinamik e-posta metinleri oluşturabilirsiniz. E-posta adreslerini ER içerisinde iki şekilde yapılandırabilirsiniz. Yapılandırma, Finance and Operations içerisindeki Yazdırma yönetiminin tamamladığı gibi aynı şekilde tamamlanabilir. Alternatif olarak, bir e-posta adresini doğrudan ER yapılandırmasını referans göstererek bir e-posta adresini çözebilirsiniz.

### <a name="email-address-types"></a>E-posta adresi türleri

**Giden** veya **CC** alanı için **Düzenle** üzerine tıkladığınızda **E-posta at** iletişim kutusu görüntülenir. Daha sonra kullanılacak e-posta adresi türünü seçebilirsiniz.

[![E-posta gönder iletişim kutusu](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Yazdırma yönetimi

**Yazdırma Yönetimi e-postası** türünü seçerseniz, **Giden** alanına sabit bir e-posta adresi girebilirsiniz. Sabit olmayan e-posta adreslerini kullanmak amacıyla bir dosya hedefi için e-posta kaynak türünü seçmelisiniz. Aşağıdaki değerler desteklenir: **Müşteri**, **Satıcı**, **Müşteri Adayı**, **İlgili kişi**, **Rakip**, **Çalışan**, **Başvuran**, **Satıcı adayı** ve **Onaylanmamış satıcı**. Bir e-posta kaynak türü seçtikten sonra **Formül tasarımcısı** formunu açmak için **E-posta kaynak hesabı** alanının yanındaki düğmeyi kullanın. Bu formu kullanarak seçilen tarafın hesabını temsil eden bir formülü, e-posta hedefine ekleyebilirsiniz.

[![Yazdırma yönetimi e-posta türünü yapılandırma](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Formüllerin ER yapılandırmasına özgü olduğunu unutmayın. **Formül** alanında bir müşteri veya satıcı tarafı türü için belgeye özgü bir referans girin. Yazmak yerine, müşteri veya satıcı hesabını temsil eden bir veri kaynağı düğümünü bulabilir ve sonra formülü güncelleştirmek için **Veri kaynağı ekle** 'ye tıklayabilirsiniz. Örneğin, ISO 20022 Borç Transferi yapılandırmasını kullanıyorsanız bir satıcı hesabını temsil eden düğüm **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** olur. Aksi takdirde, bir formül kaydetmek için **DE-001** gibi herhangi bir dize değeri girin.

[![Formül tasarımcısı](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

**E-posta gönderilecek adres** iletişim kutusunda, e-posta kaynak hesabı için formülü kalıcı olarak silmek için **E-posta kaynak hesabı** yanında bulunan geri dönüşüm kutusuna tıklayın. Alternatif olarak, önceden kaydedilmiş bir formülü değiştirmek için formül tasarımcısını açın. E-posta adresleri atamak için **E-posta adresleri ata** iletişim kutusunu açmak için **Düzenle** üzerine tıklayın.

[![Bir e-posta hedefi için e-posta adresleri atamak](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Konfigürasyon e-postası

Kullandığınız yapılandırma, veri kaynaklarında bir e-posta adresini temsil eden bir düğüme sahipse bu e-posta türünü kullanın. Formül tasarımcısında veri kaynaklarını ve fonksiyonları, doğru şekilde biçimlendirilmiş bir e-posta adresi elde etmek için kullanabilirsiniz.

[![Bir e-posta hedefi için bir e-posta adresi veri kaynağı atamak](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Not:** Basit Posta Aktarım Protokolü (SMTP) sunucusu yapılandırılmalı ve kullanılmalıdır. SMTP sunucunuzu Finance and Operations içinde, **Sistem yönetimi** &gt; **Kurulum** &gt; **E-posta** &gt; **E-posta parametreleri** içerisinde belirtebilirsiniz.

### <a name="archive-destination"></a>Arşiv hedefi

Microsoft SharePoint klasörü veya Microsoft Azure Depolamaya çıktı göndermek için bu seçeneği kullanabilirsiniz. Seçili belge türü ile tanımlanan bir hedefe çıktı göndermek için **Etkin** değerini **Evet** olarak ayarlayın. Yalnızca grubun **Dosya** olarak ayarlandığı belge türleri seçim için kullanılabilir. Belge türlerini **Kuruluş yönetimi** &gt; **Belge yönetimi** &gt; **Belge türleri** altından tanımlarsınız. ER hedefleri için yapılandırma, belge yönetim sistemi için yapılandırma ile aynıdır.

[![Belge türleri sayfası](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Konum dosyanın kaydedildiği yeri belirler. **Arşiv** hedefi etkinleştirildikten sonra, yapılandırma yürütme sonuçları İş arşivinde kaydedilebilir. Sonuçları **Kuruluş yönetimi** &gt; **Elektronik raporlama** &gt; **Elektronik raporlama arşivlenmiş işler** içerisinde görebilirsiniz. **Not:** Finance and Operations içinde İş arşivi için bir belge türünü **Kuruluş yönetimi** &gt; **Çalışma alanları** &gt; **Elektronik raporlama** &gt; **Elektronik raporlama parametreleri** içerisinde seçebilirsiniz.

#### <a name="sharepoint"></a>SharePoint

Dosyayı belirlenen bir SharePoint klasörüne kaydedebilirsiniz. Varsayılan SharePoint sunucusunu **Kuruluş yönetimi** &gt; **Belge yönetimi** &gt; **Belge yönetim parametreleri** üzerinde, **SharePoint** sekmesinde tanımlarsınız. SharePoint klasörü yapılandırıldıktan sonra, ER çıkışının belge türü için kaydedileceği klasör olarak seçebilirsiniz. 

[![Bir SharePoint klasörünü seçme](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure Depolama

Belge türü **Arşiv dizini** olarak ayarlandığında bir dosyayı Azure Depolama'ya kaydedebilirsiniz.

### <a name="file-destination"></a>Dosya hedefi

**Etkin** seçerseniz **Evet** olarak seçerseniz, yapılandırmanın çalıştırılması bittiğinde bir açma ya da kaydetme iletişim kutusu görüntülenir.

### <a name="screen-destination"></a>Ekran hedefi

**Etkin**'i **Evet** olarak ayarlarsanız, çıktının bir önizlemesi oluşturulur. XML, TXT veya PDF gibi bazı dosya türlerini doğrudan bir tarayıcı penceresinde görüntüleyebilirsiniz. Microsoft Excel veya Word gibi diğer dosya türleri için, Microsoft Office Online hizmeti kullanılır.

### <a name="power-bi-destination"></a>Power BI hedefi

Verilerinizi Finance and Operations kurulumunuzdan Microsoft Power BI hizmetlerine aktarmak amacıyla düzenlemek için Elektronik raporlama (ER) yapılandırmanızı kullanmak için **Etkin**'i **Evet** olarak ayarlayın. Aktarılan dosyalar bu amaçla yapılandırılmış bir Microsoft SharePoint Server örneği üzerinde depolanmalıdır. Daha fazla bilgi için bkz. [Power BI'ya Finance and Operations'dan gelen verileri sağlamak için Elektronik raporlama yapılandırması kullanma](general-electronic-reporting-report-configuration-get-data-powerbi.md). **İpucu:** Varsayılan davranışı geçersiz kılmak amacıyla (bir yapılandırma için iletişim kutusu) ana çıkış bileşeni için bir hedef referansı ve bir dosya hedefi oluşturabilir ve sonra tüm hedefleri devre dışı bırakabilirsiniz.

## <a name="security-considerations"></a>Güvenlik ile ilgili hususlar
ER hedefleri için iki tür ayrıcalık ve görev kullanılır. Bir tüzel kişilik için yapılandırılan genel hedefleri koruma özelliğini bir tür denetler (yani, **Elektronik raporlama hedefleri** sayfasına erişimi denetler). Diğer tür çalışma zamanında bir uygulama kullanıcısının ER geliştirici veya ER işlev danışmanı ile yapılandırılan hedef ayarlarını geçersiz kılma yeteneğini denetler.

| Rol (AOT adı)                     | Rol adı                                  | Görev (AOT adı)                     | Görev adı                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Elektronik raporlama geliştirici             | ERFormatDestinationConfigure        | Elektronik raporlama biçimi hedefini yapılandır                |
| ERFunctionalConsultant              | Elektronik raporlama işlev danışmanı | ERFormatDestinationConfigure        | Elektronik raporlama biçimi hedefini yapılandır                |
| PaymAccountsPayablePaymentsClerk    | Borç hesapları ödeme memuru            | ERFormatDestinationRuntimeConfigure | Çalışma zamanında kullanılacak elektronik raporlama biçimi hedefini yapılandır |
| PaymAccountsReceivablePaymentsClerk | Alacak hesapları ödeme memuru         | ERFormatDestinationRuntimeConfigure | Çalışma zamanında kullanılacak elektronik raporlama biçimi hedefini yapılandır |

> [!NOTE]
> Önceki görevlerde iki ayrıcalık kullanılır. Bu ayrıcalıklar ilgili görevlerle aynı adlara sahiptir: **ERFormatDestinationConfigure** ve **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Sıkça sorulan sorular
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Elektronik yapılandırmaları içe aktardım ve bunları Elektronik raporlama yapılandırmaları sayfasında görüyorum. Ancak bunları neden Elektronik raporlama hedefleri sayfasında görmüyorum?

**Yeni**'ye tıkladığınızdan ve daha sonra **Referans** alanından bir yapılandırma seçtiğinizden emin olun. **Elektronik raporlama hedefleri** sayfasında yalnızca hedeflerin yapılandırıldığı yapılandırmaları görebilirsiniz.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Hangi Azure Depolama hesabı ve Azure Blob depolamanın kullanıldığını tanımlamanın bir yolu var mıdır?

Hayır. Belge yönetim sistemi için tanımlanan ve kullanılan varsayılan Azure Blob depolama kullanılır.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Hedef ayarlarındaki Dosyanın hedefinin amacı nedir? Bu ayar ne işe yarar?

**Dosya** hedefi bir iletişim kutusunu denetlemek için kullanılır. Bu hedefi etkinleştirirseniz veya bir yapılandırma için hedef tanımlanmamışsa bir çıkış dosyası oluşturulduktan sonra bir kaydetme veya açma iletişim kutusu görürsünüz.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>E-posta gönderebileceğim bir satıcı hesabını referans gösteren bir formül örneği verebilir misiniz?

Formül ER yapılandırmasına özgüdür. Örneğin, ISO 20022 Borç Transferi yapılandırmasını kullanırsanız ilgili satıcı hesabını almak için **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** veya **model.Payments.Creditor.Identification.SourceID** 'yi kullanabilirsiniz.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Biçim yapılandırmalarımdan biri bir klasörde gruplandırılmış birden fazla dosya içeriyor (örneğin, Klasör1 Dosya1, Dosya2 ve Dosya3'ü içeriyor). Klasör1.zip klasörünün hiçbir zaman oluşmaması, Dosya1'in e-posta ile gönderilmesi, Dosya2'nin SharePoint'e gönderilmesi ve yapılandırma çalışır çalışmaz Dosya3'ü açabilmem için hedefleri nasıl ayarlarım?

Biçiminizin ER yapılandırmalarında kullanılması ön koşuldur. Kendi biçiminiz varsa **Elektronik raporlama hedefi** sayfasını açın ve bu yapılandırma için yeni bir referans oluşturun. Sonra her bir çıkış bileşeni için bir adet olmak üzere dört dosya hedefinizin olması gerekir. İlk dosya hedefini oluşturun, buna **Klasör** gibi bir ad verin ve yapılandırmanızda klasörü gösteren bir dosya adı seçin. Sonra **Ayarlar**'a tıklayın ve tüm hedeflerin devre dışı bırakıldığından emin olun. Bu dosya hedefi için klasör oluşturulmayacaktır. Varsayılan olarak, dosyalar ve ana klasörler arasındaki hiyerarşik bağımlılıklar nedeniyle dosyalar aynı şekilde davranmayacaktır. Diğer bir deyişle, bunlar her yere gönderilemeyecektir. Bu varsayılan davranışı geçersiz kılmak için her bir dosya için bir adet olmak üzere üç dosya daha oluşturmanız gerekir. Her biri için hedef ayarlarında dosyanın gönderilmesi gereken hedefi etkinleştirmeniz gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya genel bakış](general-electronic-reporting.md)




