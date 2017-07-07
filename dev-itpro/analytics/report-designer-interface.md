---
title: "Rapor Tasarımcısı arayüzü"
description: "Bu makalede, Rapor Tasarımcısı'nda nasıl gezineceğiniz ve belirli gereksinimlerinizi karşılamak için çeşitli seçenekleri nasıl kullanacağınız açıklanmaktadır."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: aad8f2617d94e9abc77dafe96cb95f7e191873bd
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017


---

# <a name="report-designer-interface"></a>Rapor Tasarımcısı arayüzü

[!include[banner](../includes/banner.md)]


Bu makalede, Rapor Tasarımcısı'nda nasıl gezineceğiniz ve belirli gereksinimlerinizi karşılamak için çeşitli seçenekleri nasıl kullanacağınız açıklanmaktadır. 

<a name="report-designer-menu-commands"></a>Rapor Tasarımcısı menü komutları
-----------------------------

Aşağıdaki tablolarda, finansal raporlar tasarlarken kullanabileceğiniz menü komutları ve seçenekleri açıklanmıştır. Bazı menü komutları ve seçenekler sadece belirli durumlarda kullanılabilir. Örneğin, raporlama birimlerinin yükseltilmesi ve indirilmesi komutları sadece bir raporlama ağacı tanımı değiştirilirken kullanılabilir.

### <a name="file-menu"></a>Dosya menüsü

**Dosya** menüsü tüm kullanıcılara açıktır ve aşağıdaki komutları içerir.

| Komut                           | Açıklama                                                                                                                                                                                      |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Yeni                               | Yeni bir rapor tanımı, satır tanımı, sütun tanımı, raporlama ağacı tanımı, rapor grup tanımı veya klasör oluşturun. Kullanıcı rolünüze bağlı olarak ek seçenekler de bulunur. |
| Açık                              | Mevcut bir satır tanımını, sütun tanımını, raporlama ağacı tanımını veya rapor tanımını açın.                                                                                             |
| Kapalı                             | Mevcut yapı taşını kapatın.                                                                                                                                                                |
| Tümünü Kapat                         | Tüm yapı taşlarını kapatın.                                                                                                                                                                       |
| Kaydet                              | Mevcut satır tanımını, sütun tanımını, raporlama ağacı tanımını veya rapor tanımını kaydedin.                                                                                             |
| Farklı Kaydet                           | Mevcut satır tanımını, sütun tanımını, raporlama ağacı tanımını veya rapor tanımını farklı bir adla kaydedin.                                                                            |
| Özellikler                        | **Özellikler** iletişim kutusunu açın; burada bir raporun adını ve açıklamasını değiştirebilirsiniz.                                                                                                   |
| Oluştur                          | Mevcut raporu oluşturun. Bu komut, bir rapor tanımında kullanılabilir.                                                                                                                 |
| Raporu Görüntüle                       | Oluşturulan raporun en güncel sürümünü Finance and Operations'da açın. Bu komut en az bir rapor oluşturduğunuzda bir rapor tanımında kullanılabilir.                                 |
| Son Rapor Tanımları         | Kısa bir süre önce oluşturulmuş veya değiştirilmiş raporların bir listesini gösterir. Listeden bir rapor seçebilirsiniz.                                                                                    |
| Son Satır Tanımları            | Kısa bir süre önce oluşturulmuş veya değiştirilmiş satır tanımlarının bir listesini gösterir. Listeden bir satır tanımı seçebilirsiniz.                                                                    |
| Son Sütun Tanımları         | Kısa bir süre önce oluşturulmuş veya değiştirilmiş sütun tanımlarının bir listesini gösterir. Listeden bir sütun tanımı seçebilirsiniz.                                                              |
| Son Raporlama Ağacı Tanımları | Kısa bir süre önce oluşturulmuş veya değiştirilmiş raporlama ağacı tanımlarının bir listesini gösterir. Listeden bir raporlama ağacı tanımı seçebilirsiniz.                                              |
| Çıkış                              | Rapor Tasarımcısından çıkın.                                                                                                                                                                            |

### <a name="edit-menu"></a>Düzenle menüsü

**Düzenle** menüsü **Tasarımcı** veya **Yönetici** görevine sahip kullanıcılar tarafından kullanılabilir. Bu menü aşağıdaki komutları içerir.

| Komut                                | Açıklama                                                                                                                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Geri al                                   | Son eylemi geri alın.                                                                                                                                                                                              |
| Yinele                                   | Son eylemi yineleyin.                                                                                                                                                                                      |
| Kes                                    | Seçilen metni silin ve panoya kopyalayın.                                                                                                                                                            |
| Kopya                                   | Seçilen metni panoya kopyalayın.                                                                                                                                                                           |
| Yapıştır                                  | En son kesilen veya kopyalanan metni panodan ekleyin.                                                                                                                                                    |
| Temizle                                  | Seçilen yapı taşını hücresinin içeriğini silin.                                                                                                                                                           |
| Bul                                   | **Bul ve Değiştir** iletişim kutusunu açın; burada metni görünüm bölmesinde arayabilirsiniz.                                                                                                                              |
| Değiştir                                | **Bul ve Değiştir** iletişim kutusunu açın; burada metni görünüm bölmesinde arayabilir ve değiştirebilirsiniz.                                                                                                                  |
| Boyutlardan Satır Ekle            | **Boyutlardan Satır Ekle** iletişim kutusunu açın; burada satır tanımına dahil edilecek boyut değerlerini seçebileceğiniz. Bu komut, bir satır tanımında kullanılabilir.                                  |
| Satırları Yeniden Numaralandır                          | Tüm sayısal satır kodlarını yeniden numaralandırın. Bu komut, bir satır tanımında kullanılabilir.                                                                                                                                   |
| Satır Bağlantıları                              | **Satır Bağlantıları** iletişim kutusunu açın; burada satır tanımlarındaki ve raporlama ağacı tanımlarındaki veri bağlantıları için kaynakları belirleyebilirsiniz. Bu komut, bir satır tanımında kullanılabilir.                            |
| Yuvarlama Ayarı                    | **Yuvarlama Ayarları** iletişim kutusunu açın; burada yuvarlama parametrelerini tanımlayabilirsiniz. Bu komut, bir satır tanımında kullanılabilir.                                                                  |
| Boyut Kümelerini Yönet                  | **Boyut Kümeleri** iletişim kutusunu açın; burada boyut kümeleri oluşturabilir ve boyut kümelerini değiştirebilirsiniz. Bu komut, satır tanımında ya da raporlama ağacı tanımında kullanılabilir.                                              |
| Satır Ekle                             | Satır tanımına boş bir satır veya sütun tanımına boş bir üstbilgi satırı ekleyin. Bu komut satır tanımında ya da sütun tanımında kullanılabilir.                                               |
| Satır Sil                             | Seçilen satırı satır tanımından veya seçilen üstbilgi satırını sütun tanımından silin. Bu komut satır tanımında ya da sütun tanımında kullanılabilir.                                       |
| Sütun Ekle                          | Sütun tanımına boş bir sütun ekleyin. Bu komut bir sütun tanımında kullanılabilir.                                                                                                             |
| Sütun Sil                          | Sütun tanımından seçilen sütunu silin. Bu komut bir sütun tanımında kullanılabilir.                                                                                                         |
| Boyutlardan Raporlama Birimleri Ekle | **Boyutlardan Raporlama Birimleri Ekle** iletişim kutusunu açın; burada raporlama ağacı tanımına dahil edilecek boyut değerlerini seçebileceğiniz. Bu komut, bir raporlama ağacı tanımında kullanılabilir. |
| Boyut Kümesi Hiyerarşisini İçe Aktar         | **Boyut Kümesi Hiyerarşisi** iletişim kutusunu açın; burada mali verilerden bir boyut kümesi hiyerarşisini içe aktarabilirsiniz. Bu komut, ..\mali-boyutlar\boyuta bağlı bir sistem için bir raporlama ağacı tanımında kullanılabilir.  |
| Raporlama Birimi Ekle                  | Raporlama ağacı tanımına bir boş satır ekleyin. Bu komut, bir raporlama ağacı tanımında kullanılabilir.                                                                                                |
| Raporlama Birimini Sil                  | Seçilen raporlama birimi satırını raporlama ağacı tanımından silin. Bu komut, bir raporlama ağacı tanımında kullanılabilir.                                                                             |

### <a name="view-menu"></a>Görünüm menüsü

**Görünüm** menüsü tüm kullanıcılara açıktır ve aşağıdaki komutları içerir.

| Komut         | Açıklama                                                            |
|-----------------|------------------------------------------------------------------------|
| Gezinti Bölmesi | Gezinti bölmesini gösterir veya gizler.                                      |
| Araç Çubukları        | Görüntülenmesini istediğiniz araç çubuklarını seçin.                                  |
| Durum Çubuğu      | **Rapor Tasarımcısı** penceresinde durum bilgilerini gösterir veya gizler. |
| Hoş Geldiniz Sayfası    | **Hoş Geldiniz** sayfasını açar.                                             |

### <a name="format-menu"></a>Biçim menüsü

**Biçim** menüsü **Tasarımcı** veya **Yönetici** görevine sahip kullanıcılar tarafından kullanılabilir. Bu menü aşağıdaki komutları içerir.

| Komut               | Açıklama                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stiller ve Biçimlendirme | **Stiller ve Biçimlendirme** iletişim kutusunu açın; burada satır tanımlarındaki ve sütun tanımlarındaki metinler için stil oluşturabilir veya bunu değiştirebilirsiniz. Bu komut bir satır tanımında ya da bir sütun tanımında kullanılabilir. |
| Sütun Genişliği          | **Sütun Genişliğini** iletişim kutusunu açın; burada seçilen sütunun genişliğini ayarlayabilirsiniz. Bu komut bir satır tanımında, bir sütun tanımında veya bir raporlama ağacı tanımında kullanılabilir.                      |
| Gizle                  | Seçili sütunu gizler. Bu komut bir satır tanımında, bir sütun tanımında veya bir raporlama ağacı tanımında kullanılabilir.                                                                                        |
| Göster                | Seçilen sütunlar arasındaki gizli sütunları görünür hale getirir. Bu komut bir satır tanımında, bir sütun tanımında veya bir raporlama ağacı tanımında kullanılabilir.                                                      |

### <a name="company-menu"></a>Şirket menüsü

**Şirket** menüsü **Tasarımcı** veya **Yönetici** görevine sahip kullanıcılar tarafından kullanılabilir. Bu menü aşağıdaki komutları içerir.

| Komut               | Açıklama                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Şirketler             | **Şirketler** iletişim kutusunu açın; burada şirketler oluşturabilir ve şirketleri değiştirebilirsiniz.                                          |
| Yapı Taşı Grupları | **Yapı Taşı Grupları** iletişim kutusunu açın; burada yapı taşı grupları oluşturabilir ve bunları değiştirebilir, içe aktarabilir ve dışa aktarabilirsiniz. |

### <a name="go-menu"></a>Git menüsü

**Git** menüsü tüm kullanıcılara açıktır ve aşağıdaki komutları içerir. **Not:** Gezinti bölmesi görünür değilse, bu komutların görünür bir etkisi olmayacaktır.

| Komutlar                   | Açıklama                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Rapor Tanımları         | Rapor tanımlarını gezinti bölmesinde gösterir.                                    |
| Satır Tanımları            | Satır tanımlarını gezinti bölmesinde gösterir.                                       |
| Sütun Tanımları         | Sütun tanımlarını gezinti bölmesinde gösterir.                                    |
| Raporlama Ağacı Tanımları | Raporlama ağacı tanımlarını gezinti bölmesinde gösterir.                            |
| Güvenlik                   | Gezinti Bölmesinde kullanıcılar, gruplar ve şirketler için güvenlik bilgilerini gösterir. |

### <a name="tools-menu"></a>Araçlar menüsü

**Araçlar** menüsü tüm kullanıcılar tarafından kullanılabilir, ancak bazı komutların kullanılabilirliği sınırlıdır. Bu menü aşağıdaki komutları içerir.

| Komut                       | Açıklama                                                                                                                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Koruma                       | Mevcut yapı taşına bir parola uygular. Bu komut, **Tasarımcı** veya **Yönetici** görevine sahip kullanıcılar tarafından kullanılabilir.                                                                           |
| Rapor Sırası Durumu           | **Rapor Sırası Durumu** iletişim kutusunu açın; burada kısa süre önce oluşturulmuş tüm raporları ve her bir raporun ayrıntılarını görebilirsiniz.                                                                                    |
| Kaynak Sistemi Bilgileri     | Microsoft Dynamics ERP sisteminiz için ayarları gösterir. Bu komut, **Tasarımcı** veya **Yönetici** görevine sahip kullanıcılar tarafından kullanılabilir.                                                                 |
| Kullanıma Alınan Maddeler             | Mevcut durumda açık olan satır tanımlarını, sütun tanımları, raporlama ağacı tanımları ve rapor tanımlarını gösterir. Bu komut, **Tasarımcı** veya **Yönetici** görevine sahip kullanıcılar tarafından kullanılabilir. |
| Önbelleğe Alınan Mali Verileri Yenile | Mali boyutlar sütunundaki verileri güncelleştirir.                                                                                                                                                               |
| Seçenekler                       | **Seçenekler** iletişim kutusunu açın; burada Rapor Tasarımcısı için kullanıcı tercihlerini değiştirebilirsiniz.                                                                                                                        |

### <a name="window-menu"></a>Pencere menüsü

**Pencere** menüsü tüm kullanıcılara açıktır ve aşağıdaki komutları içerir.

| Komut              | Açıklama                                                                                                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Yatay Döşe    | Tüm açık pencereleri yan yana gösterir.                                                                                                                                                     |
| Düşey Döşe      | Tüm açık pencereleri üst üste gösterir.                                                                                                                                               |
| Basamaklandır              | Tüm açık pencereleri, her bir pencerenin başlık çubuğu görünecek şekilde dizer.                                                                                                                      |
| Yatay Dondur    | Seçilen satırı, sayfa kaydırıldıkça satır, pencerede görünür olacak şekilde dondurur. Bu komut, **Tasarımcı** veya **Yönetici** görevine sahip kullanıcılar tarafından kullanılabilir.       |
| Düşey Dondur      | Seçilen sütunu, sayfa kaydırıldıkça sütun, pencerede görünür olacak şekilde dondurur. Bu komut, **Tasarımcı** veya **Yönetici** görevine sahip kullanıcılar tarafından kullanılabilir. |
| Açık Pencereler Listesi | Açık pencerelerin bir listesini gösterir. Öne getirmek istediğiniz pencereyi seçin.                                                                                                               |

### <a name="help-menu"></a>Yardım menüsü

**Yardım** menüsü tüm kullanıcılara açıktır ve aşağıdaki komutları içerir.

| Komut | Açıklama                                                  |
|---------|--------------------------------------------------------------|
| Yardım    | Finansal raporlama için Finance and Operations yardım konu sayfasını açın. |
|         |                                                              |

## <a name="report-designer-toolbar-buttons"></a>Rapor Tasarımcısı araç çubuğu düğmeleri
Aşağıdaki tablolarda rapor tasarlarken kullanabileceğiniz araç çubuğu düğmeleri açıklanmıştır. Bazı araç çubuğu düğmeleri sadece belirli durumlarda kullanılabilir. Örneğin, raporlama birimlerinin yükseltilmesi ve indirilmesi düğmeleri sadece bir raporlama ağacı tanımı değiştirilirken kullanılabilir.

### <a name="standard-toolbar"></a>Standart araç çubuğu

Standart araç çubuğundan dosya ve düzenleme komutlarına hızlı şekilde erişilebilir. Bu araç çubuğu aşağıdaki düğmeleri içerir.

| Düğme                                                                                                                                                                                   | Açıklama                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![Yeni düğme](./media/rowc130389.png)](./media/rowc130389.png)                              | Yeni bir (boş) rapor tanımı, satır tanımını, sütun tanımını veya raporlama ağacı tanımını oluşturun.                                                                               |
| [![Aç düğmesi](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Mevcut bir satır tanımını, sütun tanımını, raporlama ağacı tanımını veya rapor tanımını açın.                                                                                   |
| [![Kaydet düğmesi](./media/savec130389.png)](./media/savec130389.png)                           | Mevcut satır tanımını, sütun tanımını, raporlama ağacı tanımını veya rapor tanımını kaydedin.                                                                                   |
| [![Kopyala düğmesi](./media/copyc130389.png)](./media/copyc130389.png)                           | Seçilen metni panoya kopyalayın.                                                                                                                                               |
| [![Kes düğmesi](./media/cutc130389.png)](./media/cutc130389.png)                              | Seçilen metni silin ve panoya kopyalayın.                                                                                                                                |
| [![Yapıştır düğmesi](./media/pastec130389.png)](./media/pastec130389.png)                        | Metni panodan ekleyin.                                                                                                                                                    |
| [![Geri Al düğmesi](./media/undoc130389.png)](./media/undoc130389.png)                           | Son eylemi geri alın.                                                                                                                                                                  |
| [![Yinele düğmesi](./media/redoc130389.png)](./media/redoc130389.png)                           | Son eylemi yineleyin.                                                                                                                                                          |
| [![Bul düğmesi](./media/findc130389.png)](./media/findc130389.png)                           | **Bul ve Değiştir** iletişim kutusunu açın; burada aktif penceredeki metni arayabilir ve değiştirebilirsiniz.                                                                                  |
| [![Satır ekle düğmesi](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Satır tanımına boş bir satır veya sütun tanımına boş bir üstbilgi satırı ekleyin. Bu düğme bir satır tanımında ya da bir sütun tanımında kullanılabilir.                    |
| [![Sütun ekle düğmesi](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Sütun tanımına boş bir sütun ekleyin. Bu düğme bir sütun tanımında kullanılabilir.                                                                                  |
| [![Kilitle düğmesi](./media/lockc130389.png)](./media/lockc130389.png)                           | Mevcut yapı taşına bir parola uygular. Bu düğme, **Tasarımcı** veya **Yönetici** görevine sahip kullanıcılar tarafından kullanılabilir.                                                 |
| [![Satır bağlantısı düğmesi](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | **Satır Bağlantıları** iletişim kutusunu açın; burada satır tanımlarındaki ve raporlama ağacı tanımlarındaki veri bağlantıları için kaynakları belirleyebilirsiniz. Bu düğme bir satır tanımında kullanılabilir. |
| [![Yükselt düğmesi](./media/promotec130389.png)](./media/promotec130389.png)                  | Raporlama ağacı tanımındaki bir birimi yükseltir. Bir alt birim seçtikten sonra **Yükselt** düğmesini tıklarsanız alt birim, ana birimle aynı düzeye taşınır.                |
| [![Alçalt düğmesi](./media/demotec130389.png)](./media/demotec130389.png)                     | Raporlama ağacı tanımındaki bir birimi alçaltır. Bir birim seçtikten sonra **Alçalt** düğmesini tıklarsanız birim, takip eden birimin bir alt birimi haline gelir.                               |
| [![Genişlet düğmesi](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Raporlama ağacı tanımının seçilen birim düzeyindeki tüm birimlerini genişletir.                                                                                                   |
| [![Daralt düğmesi](./media/collapsec130389.png)](./media/collapsec130389.png)               | Raporlama ağacını daraltır.                                                                                                                                                           |
| [![Yardım düğmesi](./media/helpc130389.png)](./media/helpc130389.png)                           | Yardım'ı açın.                                                                                                                                                                             |

### <a name="formatting-toolbar"></a>Biçimlendirme araç çubuğu

Biçimlendirme araç çubuğu, stil komutlarına kolay erişim sağlar. Bu araç çubuğu aşağıdaki düğmeleri içerir.

| Düğme                                                                                                                                                                                                   | Açıklama                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [![Yazı tipi stili düğmesi](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Mevcut metne seçilen yazı tipi stilini uygular.      |
| [![Yazı tipi düğmesi](./media/fonttype.png)](./media/fonttype.png)                                                 | Mevcut metni seçilen yazı tipine ayarlar.              |
| [![Yazı tipi boyutu düğmesi](./media/fontsize.png)](./media/fontsize.png)                                            | Mevcut metni seçilen yazı tipi boyutuna (punto cinsinden) ayarlar. |
| [![Kalın düğmesi](./media/boldc130389.png)](./media/boldc130389.png)                                           | Mevcut metni kalın yapar.                             |
| [![İtalik düğmesi](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Mevcut metni italik yapar.                           |
| [![Alt çizgi düğmesi](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Mevcut metni altı çizili hale getirir.                             |
| [![Girintiyi azalt düğmesi](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Mevcut metnin girintisini azaltır.                |
| [![Girintiyi artır düğmesi](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Mevcut metnin girintisini artırır.                |
| [![Arkaplan rengi düğmesi](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Mevcut hücrenin arkaplan rengini değiştirir.        |
| [![Yazı tipi rengi düğmesi](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Mevcut metnin rengini değiştirir.                   |

### <a name="report-designer-toolbar"></a>Rapor tasarımcısı araç çubuğu

Rapor tasarımcısı araç çubuğu, rapor tasarımcısı içinde gezinmek için komutlara hızlı erişim sağlar. Bu araç çubuğu aşağıdaki düğmeleri içerir.

| Düğme                                                                                                                                                                                          | Açıklama                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![Rapor tanımı düğmesi](./media/reportc130389.png)](./media/reportc130389.png)                 | **Pencere** menüsünde listelenen rapor tanımını gösterir.                                                                                                            |
| [![Satır tanımını düğmesi](./media/rowc130389.png)](./media/rowc130389.png)                          | Aktif rapor tanımına atanan satır tanımını gösterir.                                                                                                    |
| [![Sütun tanımı düğmesi](./media/columnc130389.png)](./media/columnc130389.png)                 | Aktif rapor tanımına atanan sütun tanımını gösterir.                                                                                                 |
| [![Raporlama ağacı tanımı düğmesi](./media/treec130389.png)](./media/treec130389.png)             | Aktif rapor tanımına atanan raporlama ağacı tanımını gösterir.                                                                                         |
| [![Rapor Görüntüleyicisi düğmesi](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Rapor Görüntüleyicisini başlatır ve oluşturulan raporun en güncel sürümünü gösterir. Bu düğme en az bir rapor oluşturduğunuzda bir rapor tanımında kullanılabilir. |
| [![Rapor oluştur düğmesi](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Aktif rapor tanımından bir rapor oluşturur. Bu düğme bir rapor tanımında kullanılabilir.                                                                      |



<a name="see-also"></a>Ayrıca bkz.
--------

[Mali raporlama](financial-reporting-intro.md)

[Mali rapor oluşturma](generate-financial-report.md)




