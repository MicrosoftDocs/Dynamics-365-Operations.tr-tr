---
title: Kaldırılan veya artık kullanılmayan Platform özellikleri
description: Bu konu, Finance and Operations uygulamalarının platofrm güncellemelerinde kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: sericks007
manager: AnnBe
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 51d1d0ed2ce95573ec123121999d73446a7e4ea4
ms.sourcegitcommit: 6e0d6d291d4881b16a677373f712a235e129b632
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "3971457"
---
# <a name="removed-or-deprecated-platform-features"></a>Kaldırılan veya artık kullanılmayan Platform özellikleri

[!include [banner](../includes/banner.md)]

Bu konu, Finance and Operations uygulamalarının platofrm güncellemelerinde kaldırılmış veya kaldırılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır. 

Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) raporları altından ulaşabilirsiniz. Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Finance and Operations uygulamalarının 10.0.15 sürümü için platform güncelleştirmeleri

> [!NOTE]
> Sürüm 10.0.15 bir önizleme sürümüdür. İçerik ve işlevde değişiklik yapılabilir. Önizleme sürümleri hakkında daha fazla bilgi için bkz. [Bir sürüm hizmeti güncelleştirmeleriyle ilgili SSS](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).

### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Meta veri düzeltmelerini uygulamak için Visual Studio eklentisi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Meti veri düzeltmeleri artık Temmuz 2018'de 8.1 sürümüyle sunulan [One Version](../../fin-ops/get-started/one-version.md) hizmet güncelleştirmeleriyle desteklenmemektedir. |
| **Başka bir özellikle mi değiştirildi?**   | Desteklenen sürümler için bağımsız meta veri düzeltmeleri yoktur. Bunun yerine toplu kalite güncelleştirmeleri uygulanır. |
| **Etkilenen ürün alanları**         | Visual Studio eklentileri |
| **Dağıtım seçeneği**              | Geliştirme sanal makineleri |
| **Durum**                         | Sürüm 10.0.15 ile eklenti artık Visual Studio araçlarına dahil değildir. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Finance and Operations uygulamalarının 10.0.14 sürümü için platform güncelleştirmeleri

> [!NOTE]
> Sürüm 10.0.14 bir önizleme sürümüdür. İçerik ve işlevde değişiklik yapılabilir. Önizleme sürümleri hakkında daha fazla bilgi için bkz. [Hizmet güncelleştirmesi kullanılabilirliği](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/public-preview-releases).


### <a name="online-users-page"></a>Çevrimiçi kullanıcılar sayfası 

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu, önceki istemci/sunucu mimarisi için oluşturulmuş eski bir sayfadır. Bu sayfadaki bilgiler her zaman doğru değildir ve karıştırıcı ve yanıltıcı olabilir. |
| **Başka bir özellikle mi değiştirildi?**   | Gelecekteki bir güncelleştirmede yeni bir sayfa sağlayacağız.|
| **Etkilenen ürün alanları**         | Sistem Yönetimi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | 2021 Ekim'de bu form kaldırılacaktır.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Finance and Operations uygulamalarının 10.0.13 sürümü için platform güncelleştirmeleri


### <a name="custom-code-defined-in-ssrs-report-properties"></a>SSRS rapor özelliklerinde tanımlanan özel kod 

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Genel olarak, özel kod sınırlı avantaj sunarken destek için önemli miktarda kaynak kullanımı ve işlem gerektirir. Özel kod, öncelikle özel bir kod derlemesinden genel yöntemleri çağırmak için rapor yazarları tarafından kullanılır. Ancak, bulutta barındırılan hizmet SSRS raporları için özel derlemelere yönelik başvuruları desteklemez. |
| **Başka bir özellikle mi değiştirildi?**   | Rapor yazarları, herhangi bir metin kutusu ifadesinden Matematik, Dönüştürme ve Biçim işlemleri için genel .NET API'larına başvuruda bulunmaya devam etmeyi seçebilirler. Daha fazla bilgi için bkz. [Rapora Kod Ekleme (SSRS)](https://docs.microsoft.comsql/reporting-services/report-design/add-code-to-a-report-ssrs?view=sql-server-ver15).  |
| **Etkilenen ürün alanları**         | Özel kod içeren RDL'de tanımlanan uygulama raporu tasarımlarının alt kümesi. |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Sürüm 10.0.13 ile, derleyici bir SSRS rapor tanımında özel kodun algılandığı durumlar için uyarı vermeyi başlayacaktır. Sorunu gidermek için rapor tasarımı tanımını açın ve tüm özel kod yapılarını kaldırın. Bu uyarı gelecekteki bir güncelleştirmede bulunan bir derleyici hatasıyla değiştirilecektir.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Üç jQuery bileşen kitaplığını yükseltme 

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Üç jQuery bileşen kitaplığı güvenlik düzeltmeleri ve para birimini koruma açısından güncelleştirilmektedir.   
| **Başka bir özellikle mi değiştirildi?**   | Aşağıdaki kitaplıklar etkilenmiştir: jQuery (3.5.0 sürümünden 2.1.4 sürümüne kadar), jQuery UI (1.12.1 sürümünden 1.11.4 sürümüne kadar), jQuery Qtıp (2.2.1 sürümünden 3.0.3 sürümüne kadar). Geçiş kılavuzu, jQuery tarafından çevrimiçi olarak sağlanmıştır.  |
| **Etkilenen ürün alanları**         | Genişletilebilir denetimler, özellikle özel JavaScript kod kullanımı kullanım dışı bırakıldı veya API'lar kaldırıldı |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Sürüm 10.0.13/Platform güncelleştirmesi 37 ile, müşteriler isteğe bağlı olarak "üç jQuery bileşen kitaplığını yükselt" özelliğini etkinleştirerek en son kitaplıklara geçiş yapabilir. Etkilenen API'ların taşınması için zaman vermek amacıyla, yeni kitaplıklara geçiş Nisan 2021 sürümü ile zorunlu olacaktır.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Varolan kılavuz denetimi/forceLegacyGrid() API

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Varolan kılavuz denetimi yeni kılavuz denetimiyle değiştiriliyor. |
| **Başka bir özellikle mi değiştirildi?**   | [Yeni kılavuz denetimi](../..//fin-ops/get-started/grid-capabilities.md) |
| **Etkilenen ürün alanları**         | Web istemcisi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Sürüm 10.0.13'te, yeni kılavuz denetimi genellikle kullanılabilirdir ve müşteriler isteğe bağlı olarak bu özelliği açabilir. Yeni kılavuz denetimi Ekim 2021 sürümünde zorunlu olacaktır. Yeni kılavuz denetimi zorunlu hale geldiğinde **forceLegacyGrid()** API kabul edilmeyecek. |

### <a name="personalization-without-saved-views"></a>Kaydedilmiş görünümler olmadan kişiselleştirme 

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Kişiselleştirme alt sistemi, çok daha iyi performansa sahip olması ve ek özellikler sunması için kaydedilmiş görünümler özelliğiyle yenilendi. |
| **Başka bir özellikle mi değiştirildi?**   | Kayıtlı görünümler |
| **Etkilenen ürün alanları**         | Web istemcisi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Sürüm 10.0.13/Platform güncelleştirmesi 37'de, kaydedilmiş görünümler özelliği genellikle kullanılabilirdir ve müşteriler isteğe bağlı olarak bu özelliği açabilir. Kaydedilmiş görünüm özelliği Ekim 2021 sürümünde zorunlu olacaktır. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Finance and Operations uygulamalarının 10.0.12 sürümü için platform güncelleştirmeleri

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Geçersiz alan başvurularını içeren kılavuz veya Grup denetimi formu uzantıları

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Kılavuz veya grup denetimlerindeki veri grubu özelliği, bir alan grubunun tüm alanlarını otomatik olarak göstermek için kullanılır. Uzantıya göre eklenen bir kılavuz veya Grup denetimi, alan grubunda artık tanımlanmamış alanlar içerebilir veya alan grubunda tanımlanmış alanlar eksik olabilir. Bu durum çalışma zamanında tutarsız davranışlara neden olabilir. Finance and Operations uygulamalarının 10.0.12 sürümü için platform güncelleştirmeleri bu sorunu bir derleyici *uyarı* olarak sınıflandırır. Bu sorunu gidermek için, form uzantısını açın ve kaydedin.
| **Başka bir özellikle mi değiştirildi?**   | Bu derleyici uyarısı gelecekteki bir güncelleştirmede bulunan bir derleyici hatasıyla değiştirilecektir. |
| **Etkilenen ürün alanları**         | Visual Studio geliştirme araçları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Derleyici uyarısı, Finance and Operations uygulamalarının 10.0.12 sürümü platform güncelleştirmelerinde bir derleyici hatasıdır. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Finance and Operations uygulamalarının 10.0.11 sürümü için platform güncelleştirmeleri

### <a name="explicit-safe-lists-for-self-service-environments"></a>Self servis ortamları için açık güvenli listeler

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | IP'yi güvenli listelere taşıma işlemi değiştirildi. Self servis artık IP güvenli listelerini desteklemiyor. |
| **Başka bir özellikle mi değiştirildi?**   | Daha fazla bilgi için, bkz [Azure Active Directory Koşullu Erişimi yapılandırma](https://docs.microsoft.com/appcenter/general/configuring-aad-conditional-access).|
| **Etkilenen ürün alanları**         | Güvenlik |
| **Dağıtım seçeneği**              | Bulut |
| **Durum**                         | **Kullanım dışı:** Bu özellik self servis dağıtımları için tam olarak kullanım dışıdır. |

### <a name="visual-studio-2015"></a>Visual Studio2015

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Visual Studio'Nin en son sürümlerini desteklemek için Visual Studio için X++ uzantılarında bazı değişiklikler yapılmalıdır . Bu değişiklikler Visual Studio 2015 ile uyumsuz . |
| **Başka bir özellikle mi değiştirildi?**   | Visual Studio 2017, Dağıtılmış ve gerekli sürüm olarak Visual Studio 2015 yerine çalışacak. |
| **Etkilenen ürün alanları**         | Visual Studio geliştirme araçları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Visual Studio 2017 ile yeni sanal makinelerin (VM) kullanılabilirliği bildirildikten sonra, yalnızca Visual Studio 2015 olan var olan VM'Lerin sürüm dalga 2021 1 ' i tarafından yeniden dağıtılması gerekecektir. |

### <a name="field-groups-containing-invalid-field-references"></a>Geçersiz alan referansı içeren alan denetimleri

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tablo meta veri tanımlarındaki alan grupları, geçersiz alan referansları içerebilir. Bu alan grupları dağıtılırsa, Financial Reporting ve  Microsoft SQL Server Reporting Services (SSRS) içinde çalışma zamanı hatalarına neden olabilir. Platform güncelleştirmesi 23, bu meta veri veri sorununun giderilmesi için bir derleyici *uyarısı* getirdi. Finance and Operations uygulamalarının 10.0.11 sürümü için platform güncelleştirmeleri bu sorunu bir derleyici *hatası*olarak sınıflandırır.<p>Bu sorunu düzeltmek için şu adımları izleyin.</p><ol><li>Geçersiz alan referansını tablo alanı grubu tanımından kaldırın.</li><li>Yeniden derleyin.</li><li>Hataların giderildiğinden emin olun.</li></ol> |
| **Başka bir özellikle mi değiştirildi?**   | Bu derleyici hatası, derleyici uyarısının kalıcı olarak yerini alır.  |
| **Etkilenen ürün alanları**         | Visual Studio geliştirme araçları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | **Kullanım dışı:** Derleyici uyarısı, Finance and Operations uygulamalarının 10.0.11 sürümü platform güncelleştirmelerinde bir derleyici hatasıdır. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>SHA1 karma algoritması kullanılarak oluşturulan ISV lisansları

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bağımsız yazılım satıcısı (ISV) lisansları oluşturma işlemi değişti. Daha fazla bilgi için bkz. [Bağımsız yazılım satıcısı (ISV) lisansı](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Başka bir özellikle mi değiştirildi?**   | Evet. Lisans oluşturmak için Windows PowerShell'i kullanın. |
| **Etkilenen ürün alanları**         | Visual Studio geliştirme araçları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | <strong>Kullanım dışı:</strong> SHA1 karma algoritması kullanılarak oluşturulan ISV lisansları. Bu algoritma MakeCert yardımcı programı kullanılarak oluşturulan sertifikalara bağımlıydı ve bu yardımcı program kullanım dışı bırakıldı.<p><strong>Kullanım dışı:</strong> Güvenlik veya karma amaçlar için SHA1 kullanımı. SHA1 işlevi, 2021'in ilk dönemlerinde sonlandırılacaktır. Bu nedenle, artık kullanılmamalıdır.<p><strong>Kaldırıldı:</strong> Aktarım Katmanı Güvenliği (TLS) 1.0 ve TLS 1.1 gelen veya giden istekleri için destek. |

## <a name="platform-update-32"></a>Platform update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>İş akışı isteği değişikliği iletişim kutusu artık kullanıcı seçimi açılan listesini içermiyor
|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Değişiklik isteği istenmeyen bir kullanıcıya gönderilebileceğinden bu bir güvenlik sorunudur. Bu aynı zamanda bir kullanılabilirlik sorunudur ve kullanıcıyı iş akışının kaynağını belirlemeye ve bunları el ile seçmelerine olanak sağlar.  |
| **Başka bir özellikle mi değiştirildi?**   | Hayır |
| **Etkilenen ürün alanları**         | İş akışı |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanıcı seçimi açılan listesi, platform güncelleştirmesi 32 ' deki istek değişimi iletişim kutusundan kaldırıldı. İstek değişikliği istekleri oluşturana otomatik olarak istendiği gibi gönderilecek. Bu işlevsellik hakkında daha fazla bilgi için bkz [İş akışı onay sürecindeki eylemler](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Katıştırılmış ayrıntılandırma bağlantıları bulut tarafından barındırılan hizmet tarafından işlenen sayfalandırılmış belgelerde artık desteklenmiyor 
|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Hizmet tarafından işlenen belgelere katıştırılmış olan gezinti URL'leri hassas iş verileri içerebilir. Müşteri verilerini daha iyi korumak amacıyla bir güvenlik önlemi olarak belgelerdeki katıştırılmış ayrıntılandırma bağlantıları için desteği kaldırıyoruz. Kullanıcılar ayrıca, bu değişikliğin sonucunda etkileşimli olarak belge oluştururken gelişmiş performanstan da yararlanacaktır.  |
| **Başka bir özellikle mi değiştirildi?**   | No |
| **Etkilenen ürün alanları**         | Raporlama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Bu özellik, hizmetten etkin olarak kaldırılmaktadır.<br><br>Modern istemci, uygulamada gezinme konusunda yardımcı olacak otomatik oluşturulmuş bağlantılar içeren görünümler üretmek için birçok seçenek sunar. Hizmet tarafından işlenen sayfalandırılmış belgeler e-postayla gönderilen, arşivlenen ve alıcılar için yazdırılan harici iletişimler için önerilir. Belgeleri doğrudan tarayıcıda önizleme deneyimini geliştirdik (yerel yazıcılara doğrudan erişim sunar). Daha fazla bilgi için bkz. [Katıştırılmış görüntüleyiciyle PDF belgelerini önizleme](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular
Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../migration-upgrade/deprecated-features.md) bakın.

