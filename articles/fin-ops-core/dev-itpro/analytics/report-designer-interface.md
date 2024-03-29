---
title: Rapor Tasarımcısı arayüzü
description: Bu makalede, Report Designer'da nasıl gezineceğiniz ve belirli gereksinimlerinizi karşılamak için çeşitli seçenekleri nasıl kullanacağınız açıklanmaktadır.
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.form: FinancialReports
ms.openlocfilehash: 25d913e6f5d4c95dceda1291a2c33abe37348574
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802755"
---
# <a name="report-designer-interface"></a>Rapor Tasarımcısı arayüzü

[!include [banner](../includes/banner.md)]

Bu makalede, Report Designer'da nasıl gezineceğiniz ve belirli gereksinimlerinizi karşılamak için çeşitli seçenekleri nasıl kullanacağınız açıklanmaktadır.

## <a name="report-designer-menu-commands"></a>Report Designer menü komutları

Aşağıdaki tablolarda, finansal raporlar tasarlarken kullanabileceğiniz menü komutları ve seçenekleri açıklanmıştır. Bazı menü komutları ve seçenekler sadece belirli durumlarda kullanılabilir. Örneğin, raporlama birimlerini yükseltme ve indirgeme komutlarını yalnızca bir raporlama ağacı tanımını değiştirirken kullanabilirsiniz.

### <a name="file-menu"></a>Dosya menüsü

**Dosya** menüsü tüm kullanıcılar tarafından kullanılabilir ve aşağıdaki komutları içerir.

| Komut                           | Açıklama |
|-----------------------------------|-------------|
| Yeni                               | Yeni bir rapor tanımı, satır tanımı, sütun tanımı, raporlama ağacı tanımı, rapor grup tanımı veya klasör oluşturun. Kullanıcı rolünüze bağlı olarak ek seçenekler de bulunur. |
| Açık                              | Var olan bir satır tanımı, sütun tanımı, raporlama ağacı tanımı veya rapor tanımını açın. |
| Kapanış                             | Geçerli yapı taşını kapatın. |
| Tümünü kapat                         | Tüm yapı taşlarını kapatın. |
| Kaydet                              | Geçerli satır tanımı, sütun tanımı, raporlama ağacı tanımı veya rapor tanımını kaydedin. |
| Farklı kaydet                           | Geçerli satır tanımı, sütun tanımı, raporlama ağacı tanımı veya rapor tanımını yeni bir adla kaydedin. |
| Özellikler                        | **Özellikler** iletişim kutusunu açın. Burada bir raporun adını ve açıklamasını değiştirebilirsiniz. |
| Oluştur                          | Geçerli raporu oluşturun. Bu komut bir rapor tanımından kullanılabilir. |
| Raporu görüntüle                       | Oluşturulan raporun en güncel sürümünü açın. Bu komut en az bir rapor oluşturduğunuzda bir rapor tanımında kullanılabilir. |
| Son rapor tanımları         | Yeni oluşturulan veya değiştirilen raporların listesini gösterin. Ardından listeden bir rapor seçebilirsiniz. |
| Son satır tanımları            | Yeni oluşturulan veya değiştirilen satır tanımlarının listesini gösterin. Ardından listeden bir satır tanımı seçebilirsiniz. |
| Son sütun tanımları         | Yeni oluşturulan veya değiştirilen sütun tanımlarının listesini gösterin. Ardından listeden bir sütun tanımı seçebilirsiniz. |
| Yeni raporlama ağacı tanımları | Yeni oluşturulan veya değiştirilen raporlama ağacı tanımlarının listesini gösterin. Ardından listeden bir raporlama ağacı tanımı seçebilirsiniz. |
| Çık                              | Rapor Tasarımcısı'ndan çıkın. |

### <a name="edit-menu"></a>Düzenle menüsü

**Düzenle** menüsünü **Tasarımcı** veya **Yönetici** rolüne sahip kullanıcılar kullanabilir. Bu menü aşağıdaki komutları içerir.

| Komut                                | Açıklama |
|----------------------------------------|-------------|
| Geri Al                                   | Son eylemi geri alın. |
| Yeniden Yap                                   | Son geri alma eylemini tersine çevirin. |
| Kes                                    | Seçilen metni silin ve panoya kopyalayın. |
| Kopyala                                   | Seçilen metni panoya kopyalayın. |
| Yapıştır                                  | En son kesilen veya kopyalanan metni panodan ekleyin. |
| Temizle                                  | Seçilen yapı taşı hücresinin içindekileri silin. |
| Bul                                   | **Bul ve Değiştir** iletişim kutusunu açın. Burada görüntüleme bölmesindeki metinde arama yapabilirsiniz. |
| Değiştir                                | **Bul ve Değiştir** iletişim kutusunu açın. Burada görüntüleme bölmesindeki metinde arama ve değiştirme işlemi yapabilirsiniz. |
| Boyutlardan satır ekle            | **Boyutlardan Satır Ekle** iletişim kutusunu açın. Burada satır tanımına eklemek üzere boyut değerlerini seçebilirsiniz. Bu komut bir satır tanımından kullanılabilir. |
| Satırları yeniden numaralandır                          | Tüm sayısal satır kodlarını yeniden numaralandırın. Bu komut bir satır tanımından kullanılabilir. |
| Satır bağlantıları                              | **Satır Bağlantıları** iletişim kutusunu açın. Burada satır tanımları ve raporlama ağacı tanımlarındaki veri bağlantılarının kaynaklarını belirtebilirsiniz. Bu komut bir satır tanımından kullanılabilir. |
| Yuvarlama ayarlama                    | **Yuvarlama Ayarlamaları** iletişim kutusunu açın. Burada yuvarlama parametrelerini belirtebilirsiniz. Bu komut bir satır tanımından kullanılabilir. |
| Boyut kümelerini yönet                  | **Boyut Kümeleri** iletişim kutusunu açın. Burada boyut kümeleri oluşturup bunları değiştirebilirsiniz. Bu komut bir satır tanımından veya raporlama ağacı tanımından kullanılabilir. |
| Satır ekle                             | Satır tanımına boş bir satır veya sütun tanımına boş bir başlık satırı ekleyin. Bu komut bir satır tanımından veya sütun tanımından kullanılabilir. |
| Satır sil                             | Seçilen satırı satır tanımından veya seçilen başlık satırını sütun tanımından silin. Bu komut bir satır tanımından veya sütun tanımından kullanılabilir. |
| Sütun ekle                          | Sütun tanımına boş bir sütun ekleyin. Bu komut bir sütun tanımından kullanılabilir. |
| Sütun sil                          | Seçilen sütunu sütun tanımından silin. Bu komut bir sütun tanımından kullanılabilir. |
| Boyutlardan raporlama birimleri ekle | **Boyutlardan Raporlama Birimleri Ekle** iletişim kutusunu açın. Burada raporlama ağacı tanımına eklemek üzere boyut değerlerini seçebilirsiniz. Bu komut bir raporlama ağacı tanımından kullanılabilir. |
| Boyut kümesi hiyerarşisini içe aktar         | **Boyut Kümesi Hiyerarşisi** iletişim kutusunu açın. Burada mali verilerden bir boyut kümesi hiyerarşisi aktarabilirsiniz. Bu komut, ..\\mali-boyutlar\\boyuta bağlı sistem için bir raporlama ağacı tanımında kullanılabilir. |
| Raporlama birimi ekle                  | Raporlama ağacı tanımına boş bir satır ekleyin. Bu komut bir raporlama ağacı tanımından kullanılabilir. |
| Raporlama birimini sil                  | Seçilen raporlama birimi satırını raporlama ağacı tanımından silin. Bu komut bir raporlama ağacı tanımından kullanılabilir. |

### <a name="view-menu"></a>Görüntüle menüsü

**Görüntüle** menüsü tüm kullanıcılar tarafından kullanılabilir ve aşağıdaki komutları içerir.

| Komut         | Açıklama                                                            |
|-----------------|------------------------------------------------------------------------|
| Gezinti Bölmesi | Gezinti bölmesini gösterin veya gizleyin.                                      |
| Araç Çubukları        | Görünen araç çubuklarını seçin.                                  |
| Durum Çubuğu      | **Report Designer** penceresindeki durum bilgilerini gösterin veya gizleyin. |
| Hoş Geldiniz Sayfası    | **Hoş Geldiniz** sayfasını açın.                                             |

### <a name="format-menu"></a>Biçim menüsü

**Biçim** menüsünü **Tasarımcı** veya **Yönetici** rolüne sahip kullanıcılar kullanabilir. Bu menü aşağıdaki komutları içerir.

| Command               | Açıklama |
|-----------------------|-------------|
| Stiller ve Biçimlendirme | **Stiller ve biçimlendirme** iletişim kutusunu açın. Burada satır ve sütun tanımlarındaki metnin stilini oluşturup değiştirebilirsiniz. Bu komut bir satır tanımından veya sütun tanımından kullanılabilir. |
| Sütun Genişliği          | **Sütun genişliği** iletişim kutusunu açın. Burada seçilen sütunun genişliğini ayarlayabilirsiniz. Bu komut bir satır tanımı, sütun tanımı veya raporlama ağacı tanımından kullanılabilir. |
| Gizle                  | Seçilen sütunu gizleyin. Bu komut bir satır tanımı, sütun tanımı veya raporlama ağacı tanımından kullanılabilir. |
| Göster                | Seçilen sütunlar arasındaki gizli sütunları görünür yapın. Bu komut bir satır tanımı, sütun tanımı veya raporlama ağacı tanımından kullanılabilir. |

### <a name="company-menu"></a>Şirket menüsü

**Şirket** menüsünü **Tasarımcı** veya **Yönetici** rolüne sahip kullanıcılar kullanabilir. Bu menü aşağıdaki komutları içerir.

| Komut               | Açıklama                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Şirketler             | **Şirketler** iletişim kutusunu açın. Burada şirketler oluşturup bunları değiştirebilirsiniz.                                          |
| Yapı Taşı Grupları | **Yapı taşı grupları** iletişim kutusunu açın. Burada yapı taşı grupları oluşturabilir, bunları değiştirebilir, içe ve dışa aktarabilirsiniz. |

### <a name="go-menu"></a>Git menüsü

**Git** menüsü tüm kullanıcılar tarafından kullanılabilir ve aşağıdaki komutları içerir.

> [!NOTE]
> Gezinti bölmesi görünür olmadığı sürece bu komutların görünür etkisi yoktur.

| Komutlar                   | Açıklama                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Rapor Tanımları         | Gezinti bölmesindeki rapor tanımlarını gösterin.                                    |
| Satır Tanımları            | Gezinti bölmesindeki satır tanımlarını gösterin.                                       |
| Sütun Tanımları         | Gezinti bölmesindeki sütun tanımlarını gösterin.                                    |
| Raporlama Ağacı Tanımları | Gezinti bölmesindeki raporlama ağacı tanımlarını gösterin.                            |
| Güvenlik                   | Gezinti bölmesindeki kullanıcılar, gruplar ve şirketler için güvenlik bilgilerini gösterin. |

### <a name="tools-menu"></a>Araçlar menüsü

**Araçlar** menüsü tüm kullanıcılar tarafından kullanılabilir, ancak bazı komutlar sınırlı biçimde kullanılabilir. Bu menü aşağıdaki komutları içerir.

| Komut                       | Açıklama |
|-------------------------------|-------------|
| Koru                       | Geçerli yapı taşına parola uygulayın. Bu komutu **Tasarımcı** veya **Yönetici** rolüne sahip kullanıcılar kullanabilir. |
| Rapor Kuyruğu Durumu           | **Rapor Kuyruğu Durumu** iletişim kutusunu açın. Burada yeni oluşturulan tüm raporları ve her raporun ayrıntılarını görebilirsiniz. |
| Kaynak Sistem Bilgileri     | Microsoft Dynamics ERP sisteminizin ayarlarını gösterin. Bu komutu **Tasarımcı** veya **Yönetici** rolüne sahip kullanıcılar kullanabilir. |
| Kullanıma Alınan Maddeler             | O anda açık olan satır tanımları, sütun tanımları, raporlama ağacı tanımları ve rapor tanımlarını gösterin. Bu komutu **Tasarımcı** veya **Yönetici** rolüne sahip kullanıcılar kullanabilir. |
| Ön Belleğe Alınan Mali Verileri Yenile | Mali boyutlar sütunundaki verileri güncelleştirin. |
| Seçenekler                       | **Seçenekler** iletişim kutusunu açın. Burada Rapor Tasarımcısı için kullanıcı tercihlerini değiştirebilirsiniz. |

### <a name="window-menu"></a>Pencere menüsü

**Pencere** menüsü tüm kullanıcılar tarafından kullanılabilir ve aşağıdaki komutları içerir.

| Komut              | Açıklama |
|----------------------|-------------|
| Yatay Döşe    | Tüm açık pencereleri birbirinin yanında gösterin. |
| Dikey Döşe      | Tüm açık pencereleri birbirinin üzerinde gösterin. |
| Basamaklandır              | Tüm açık pencereleri her pencerenin başlık çubuğu görünür olacak şekilde basamaklandırın. |
| Yatay Dondur    | Seçilen satırı kaydırdıkça satır pencerede görünür olmaya devam edecek şekilde dondurun. Bu komutu **Tasarımcı** veya **Yönetici** rolüne sahip kullanıcılar kullanabilir. |
| Dikey Dondur      | Seçilen sütunu kaydırdıkça sütun pencerede görünür olmaya devam edecek şekilde dondurun. Bu komutu **Tasarımcı** veya **Yönetici** rolüne sahip kullanıcılar kullanabilir. |
| Açık Pencere Listesi | Açık olan pencerelerin listesini gösterin. Öne getirmek için bir pencere seçin. |

### <a name="help-menu"></a>Yardım menüsü

**Yardım** menüsü tüm kullanıcılara açıktır ve aşağıdaki komutları içerir.

| Command | Açıklama                                                              |
|---------|--------------------------------------------------------------------------|
| Yardım    | Mali raporlama için yardım makalesi sayfasını açın. |
|         |                                                                          |

## <a name="report-designer-toolbar-buttons"></a>Report Designer araç çubuğu düğmeleri
Aşağıdaki tablolarda rapor tasarlarken kullanabileceğiniz araç çubuğu düğmeleri açıklanmıştır. Bazı araç çubuğu düğmeleri yalnızca belirli koşullarda kullanılabilir. Örneğin, raporlama birimlerini yükseltme ve indirgeme düğmelerini yalnızca bir raporlama ağacı tanımını değiştirirken kullanabilirsiniz.

### <a name="standard-toolbar"></a>Standart araç çubuğu

Standart araç çubuğu dosya ve düzenle komutlarına hızlı erişim sağlar. Bu araç çubuğu aşağıdaki düğmeleri içerir.

| Düğme                                                                                       | Tanım |
|----------------------------------------------------------------------------------------------|-------------|
| [![Yeni düğmesi.](./media/rowc130389.png)](./media/rowc130389.png)                              | Yeni (boş) bir rapor tanımı, satır tanımı, sütun tanımı veya raporlama ağacı tanımı oluşturun. |
| [![Aç düğmesi.](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Var olan bir satır tanımı, sütun tanımı, raporlama ağacı tanımı veya rapor tanımını açın. |
| [![Kaydet düğmesi.](./media/savec130389.png)](./media/savec130389.png)                           | Geçerli satır tanımı, sütun tanımı, raporlama ağacı tanımı veya rapor tanımını kaydedin. |
| [![Kopyala düğmesi.](./media/copyc130389.png)](./media/copyc130389.png)                           | Seçilen metni panoya kopyalayın. |
| [![Kes düğmesi.](./media/cutc130389.png)](./media/cutc130389.png)                              | Seçilen metni silin ve panoya kopyalayın. |
| [![Yapıştır düğmesi.](./media/pastec130389.png)](./media/pastec130389.png)                        | Metni panodan ekleyin. |
| [![Geri Al düğmesi.](./media/undoc130389.png)](./media/undoc130389.png)                           | Son eylemi geri alın. |
| [![Yinele düğmesi.](./media/redoc130389.png)](./media/redoc130389.png)                           | Son geri alma eylemini tersine çevirin. |
| [![Bul düğmesi.](./media/findc130389.png)](./media/findc130389.png)                           | **Bul ve Değiştir** iletişim kutusunu açın. Burada etkin penceredeki metinde arama ve değiştirme işlemi yapabilirsiniz. |
| [![Satır ekle düğmesi.](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Satır tanımına boş bir satır veya sütun tanımına boş bir başlık satırı ekleyin. Bu düğme bir satır tanımından veya sütun tanımından kullanılabilir. |
| [![Sütun ekle düğmesi.](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Sütun tanımına boş bir sütun ekleyin. Bu düğme bir sütun tanımından kullanılabilir. |
| [![Kilitle düğmesi.](./media/lockc130389.png)](./media/lockc130389.png)                           | Geçerli yapı taşına parola uygulayın. Bu düğmeyi **Tasarımcı** veya **Yönetici** rolüne sahip kullanıcılar kullanabilir. |
| [![Satır bağlantısı düğmesi.](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | **Satır Bağlantıları** iletişim kutusunu açın. Burada satır tanımları ve raporlama ağacı tanımlarındaki veri bağlantılarının kaynaklarını belirtebilirsiniz. Bu düğme bir satır tanımından kullanılabilir. |
| [![Yükselt düğmesi.](./media/promotec130389.png)](./media/promotec130389.png)                  | Raporlama ağacı tanımının bir birimini yükseltin. Alt birimi seçip ardından **Yükselt**'i seçtiğinizde, alt birim üst birimiyle aynı düzeye taşınır. |
| [![Alçalt düğmesi.](./media/demotec130389.png)](./media/demotec130389.png)                     | Raporlama ağacı tanımının bir birimini indirgeyin. Alt birimi seçip ardından **İndirge**'yi seçtiğinizde, birim ondan önce gelen birimin alt öğesi olur. |
| [![Genişlet düğmesi.](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Raporlama ağacı tanımının tüm birimlerini seçilen birim düzeyinde genişletin. |
| [![Daralt düğmesi.](./media/collapsec130389.png)](./media/collapsec130389.png)               | Raporlama ağacını daraltır. |
| [![Yardım düğmesi.](./media/helpc130389.png)](./media/helpc130389.png)                           | Yardım'ı açın. |

### <a name="formatting-toolbar"></a>Biçimlendirme araç çubuğu

Biçimlendirme araç çubuğu, stil komutlarına kolay erişim sağlar. Bu araç çubuğu aşağıdaki düğmeleri içerir.

| Düğme                                                                                                       | Tanım                                           |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [![Yazı tipi stili düğmesi.](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Seçilen yazı tipi stilini geçerli metne uygulayın.   |
| [![Yazı tipi düğmesi.](./media/fonttype.png)](./media/fonttype.png)                                                 | Geçerli metni seçilen yazı tipine ayarlayın.           |
| [![Yazı tipi boyutu düğmesi.](./media/fontsize.png)](./media/fontsize.png)                                            | Geçerli metni seçilen yazı tipi boyutuna (punto olarak) ayarlayın. |
| [![Kalın düğmesi.](./media/boldc130389.png)](./media/boldc130389.png)                                           | Geçerli metni kalınlaştırın.                          |
| [![İtalik düğmesi.](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Geçerli metni italik yapın.                        |
| [![Alt çizgi düğmesi.](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Geçerli metnin altını çizin.                          |
| [![Girintiyi azalt düğmesi.](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Geçerli metnin girintisini azaltın.             |
| [![Girintiyi artır düğmesi.](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Geçerli metnin girintisini artırın.             |
| [![Arkaplan rengi düğmesi.](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Mevcut hücrenin arkaplan rengini değiştirir.     |
| [![Yazı tipi rengi düğmesi.](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Mevcut metnin rengini değiştirir.                |

### <a name="report-designer-toolbar"></a>Rapor tasarımcısı araç çubuğu

Rapor tasarımcısı araç çubuğu, rapor tasarımcısı içinde gezinmek için komutlara hızlı erişim sağlar. Bu araç çubuğu aşağıdaki düğmeleri içerir.

| Düğme                                                                                              | Tanım |
|-----------------------------------------------------------------------------------------------------|-------------|
| [![Rapor tanımı düğmesi.](./media/reportc130389.png)](./media/reportc130389.png)            | **Pencere** menüsünde belirtilen rapor tanımını gösterin. |
| [![Satır tanımını düğmesi.](./media/rowc130389.png)](./media/rowc130389.png)             | Etkin rapor tanımına atanan satır tanımını gösterin. |
| [![Sütun tanımı düğmesi.](./media/columnc130389.png)](./media/columnc130389.png)  | Etkin rapor tanımına atanan sütun tanımını gösterin. |
| [![Raporlama ağacı tanımı düğmesi.](./media/treec130389.png)](./media/treec130389.png)             | Etkin rapor tanımına atanan raporlama ağacı tanımını gösterin. |
| [![Rapor Görüntüleyicisi düğmesi.](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Rapor Görüntüleyici'yi başlatın ve oluşturulan raporun en yeni sürümünü gösterin. En az bir rapor oluşturduysanız bu düğme bir rapor tanımından kullanılabilir. |
| [![Rapor oluştur düğmesi.](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Etkin rapor tanımından rapor oluşturun. Bu düğme bir rapor tanımından kullanılabilir. |

## <a name="additional-resources"></a>Ek kaynaklar

[Mali raporlama](financial-reporting-intro.md)

[Mali raporlar oluşturma](generate-financial-report.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
