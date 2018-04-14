---
title: "POS için görev kaydedici ve Yardım"
description: "Bu konu, Görev kaydedicinin Retail Modern POS ve Bulut POS içerisinde nasıl kullanılacağını açıklar."
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 12aa71843fa8b22eb7ae688ed3600168760d90da
ms.contentlocale: tr-tr
ms.lasthandoff: 03/08/2018

---

# <a name="task-recorder-and-help-for-pos"></a>POS için görev kaydedici ve Yardım

[!INCLUDE [banner](includes/banner.md)]

Bu konu, Görev kaydedicinin Retail Modern POS ve Bulut POS içerisinde nasıl kullanılacağını açıklar.

<a name="overview"></a>Özet
--------

Perakende Modern POS veya Bulut POS içerisindeki görev kaydedici, yüksek cevap verebilirliğe odaklı oluşturulmuş yeni bir çözümdür. Genişletilebilirlik ve iş işlemi kayıtlarının müşterileri ile sorunsuz tümleştirme sağlayan esnek bir uygulama programlama arabirimi (API) sağlar. Ek olarak, Microsoft Lifecycle Services üzerinde İş süreci modelleyici (BPM) aracı ile Görev kaydedici tümleştirmesi ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) ileri getirilmiştir. Bu sayede kullanıcılar, kendi uygulamalarını analiz etmek ve tasarlamak için zengin iş işlemi diyagramlarını kayıtlardan üretebilirler.

## <a name="architecture"></a>Mimari
Görev kaydedici, kullanıcı eylemlerini istemcide tam doğrulukla kaydedebilir. Her bir denetim, bir kullanıcı eyleminin gerçekleştirilmesi hakkında Görev kaydediciye bildirilmek üzere belirtilmiştir. Denetim, Görev kaydediciye bir eylemin gerçekleştiğini bildirir ve kullanıcı eylemi ile ilgili tüm geçerli bilgileri gerçek zamanlı olarak aktarır. Görev kaydedicisi, bu bilgilerden kullanıcı eyleminin türünü (örneğin düğme tıklaması, değer girişi veya gezinti) ve kullanıcı eylemiyle ilişkili tüm verileri (örneğin giriş veri değeri ve türü, form içeriği veya kayıt bağlamı) yakalayabilir. Görev kaydedici, kaydın oynatımın kaydedilen eylemleri, aynı kullanıcının yaptığı gibi oynatılmasını garanti edecek ayrıntıyla üstlenir. (Yürütme özelliği henüz Perakende modern POS veya Bulut POS'da uygulanmamıştır.)

## <a name="basic-configuration"></a>Temel yapılandırma
Görev kaydetmeyi POS'da etkinleştirmek için şu adımları izleyin.

1.  **Perakende** &gt; **Kanal Kurulumu** &gt; **POS Kurulumu** &gt; **Kayıtlar** üzerine tıklayın.
2.  Görev kaydedicinin etkinleştirileceği kaydı tıklatın.
3.  **Kayıt** sekmesinde, **Genel** hızlı sekmesi üzerinde **Görev kaydetmeyi etkinleştir** seçeneğini **Evet** olarak ayarlayın.
4.  **Kaydet**'i tıklatın.
5.  **Perakende** &gt; **Perakende BT** &gt; **Dağıtım planı** öğesine gidin.
6.  **Kayıtlar (1090)** işini seçin ve ardından **Şimdi çalıştır** düğmesini tıklayın.

## <a name="create-a-recording"></a>Bir kayıt oluştur
Görev kaydedicisini kullanarak yeni bir kayıt oluşturmak için şu adımları izleyin.

1.  Perakende Modern POS veya Bulut POS'u başlatın ve oturum açın.
2.  **Ayarlar** sayfasında, **Görev Kaydedici** bölümünde **Görev kaydediciyi aç** üzerine tıklayın. **Görev kaydedici** bölmesi görüntülenir. Yeni bir kayda başlamadan önce sağ üst köşedeki **Kapat** düğmesi (**X**) üzerine tıklayarak **Görev kaydediciyi** kapatabilirsiniz. Bölmeyi yeniden açmak için, 2. adımı tekrar edin.
[![Görev kaydedici bölmesi](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3.  Kayıt için bir ad ve açıklama girin, daha sonra **Başlat** üzerine tıklayın. Kayıt oturumu **Başlat** üzerine tıklar tıklamaz başlar.

**Not:** Kayıt sürerken sağ üst köşedeki **Kapat** düğmesine (**X**) tıklarsanız, **Görev kaydedici** bölümü kapatılır ancak kayıt oturumu sonlandırılmaz. Görev kaydedici bölmesini yeniden açmak için ekranın üst kısmındaki **Yardım** düğmesine (soru işareti) tıklayın. 

[![Soru işareti](./media/help.jpg)](./media/help.jpg)

4.  **Başlat** üzerine tıkladıktan sonra, Görev kaydedici kayıt moduna girer. **Görev kaydedici** bölmesi, kayıt işlemi hakkındaki bilgileri ve denetimleri gösterir.
5.  Perakende Modern POS veya Bulut POS kullanıcı arabirimi (UI) üzerinde gerçekleştirmek istediğiniz eylemleri gerçekleştirin.
6.  Kayıt oturumunu sonlandırmak için **Durdur** üzerine tıklayın.

## <a name="download-options"></a>İndirme seçenekleri
Kaydetme oturumunu sona erdirdikten sonra, çeşitli seçenekler gösterilir, böylece kaydınızı indirebilirsiniz. 
[![İndirme seçenekleri](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>Bu bilgisayara kaydet

Görev kılavuzunu yürütmek, kaydı düzenlemek veya kayıttaki notları düzenlemek için kayıt paketini kullanabilirsiniz. (Bu özellik Perakende Modern POS ve Bulut POS içerisinde henüz uygulanmamıştır.)

### <a name="export-as-word-document"></a>Word belgesi olarak dışa aktar

Kaydı bir Microsoft Word belgesi olarak kaydedebilirsiniz. Bu belge kaydedilen adımları ve yakalanan ekran görüntülerini içerir.

### <a name="save-as-developer-recording"></a>Geliştirici kaydı olarak kaydet

Ham kayıt dosyası, test kodu oluşturulması gibi geliştirici senaryoları için yararlıdır. (Bu özellik henüz uygulanmamıştır.)

## <a name="recording-controls"></a>Kayıt kontrolleri
### <a name="recording-controlsmediacontrolsjpgmediacontrolsjpg"></a>[![Kayıt kontrolleri](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>Durdur

Kayıt oturumunu sonlandırmak için **Durdur** üzerine tıklayın. Bir oturumu sonlandırdıktan sonra yeniden başlatamayacağınızı unutmayın. Bu nedenle, kaydı sonlandırmadan önce tamamlandığından emin olun.

### <a name="pause"></a>Duraklat

Geçici olarak durdurmak (duraklatmak) ve işleme devam etmek için **Duraklat** üzerine tıklayın. **Duraklat** üzerine tıkladıktan sonra gerçekleştirecek adımlar kaydedilmez.

### <a name="continue"></a>Devam

Duraklattıktan sonra kayıt oturumuna devam etmek için **Devam et** üzerine tıklayın.

### <a name="capture-screenshots"></a>Ekran görüntülerini yakala

Görev kaydedici, Perakende Modern POS arabirimi ekran görüntülerini, siz bir iş işlemini kaydederken yakalayabilir. Ekran görüntüsü yakalama özelliğini açmak için **Ekran görüntüsü yakala** seçeneğini **Evet** olarak ayarlayın ve ardından kaydı yapın. Kayıt tamamlandıktan sonra **Durdur**'a tıklayın ve Word belgesini indirin. Belge ilgili ekran görüntüleriyle birlikte adımları içerecektir.

#### <a name="note"></a>Not
> Ekran görüntüsü yakalama işlevi Bulut POS içerisinde desteklenmez.

### <a name="start-task-and-end-task"></a>Görevi başlat ve bitir

Gruplanan bir dizi adımın başlangıcını ve bitişini **Görevi başlat** ve **görevi** **Bitir** düğmeleri ile belirtebilirsiniz. Bir "Görevi Başlat" adımı eklemek için **Görevi başlat** üzerine tıklayın ve gruba dahil edilecek adımları gerçekleştirin. Grup için adımları gerçekleştirmeyi bitirdikten sonra **Görevi sonlandır** üzerine tıklayın. Görevler, işlemlerinizi düzenlemenize yardımcı olur. Görevler diğer görevlerle iç içe kullanılabilir. Bu şekilde, çok uzun ve karmaşık iş işlemlerini daha iyi düzenleyebilirsiniz.

## <a name="adding-annotations"></a>Ek açıklamalar ekleme
Bir ek açıklama, kayıt içerisinde bir adıma eklediğiniz ek metindir. Örneğin, kullanıcıya daha fazla bağlam ve yönerge sunmak için ek açıklamaları kullanabilirsiniz. Ek açıklamaları bir adımdan önce veya sonra ekleyebilirsiniz. Adımın sağındaki **Düzenle** düğmesine (kalem simgesi) tıklayarak herhangi bir adıma ek açıklama ekleyebilirsiniz. 

[![Bir adım için düzenle düğmesi](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>Metinler ve notlar

**Metinler** ve **Notlar** alanlarını, bir Görev kılavuzu içerisindeki bir adımla ilişkilendirilecek metin eklemek için kullanabilirsiniz.
[![Metin ve Notlar alanları](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>Metin

**Metin** alanına girdiğiniz metinler, Görev kılavuzunda adımın *üzerinde* görüntülenir. Bu konum, kullanıcının adımı tamamlamadan önce görmesini istediğiniz metinler için uygundur.

#### <a name="notes"></a>Notlar

**Notlar** alanına girdiğiniz metinler, Görev kılavuzunda adımın *altında* görüntülenir. Not metnini okumak için kullanıcının adım metnini açılan pencerede genişletmesi gerekir. Bu konum, ek okuma materyalleri ve kullanıcıya yarar sağlayabilecek ancak kullanıcının eylemi tamamlaması için zorunlu olmayan diğer bilgiler için uygundur.

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>Retail Modern POS ve Bulut POS'da yardım
Görev kayıtlarınızın Perakende Modern POS ve Bulut POS için metin olarak görüntülenebilmesi için onları Yardım bölmesinde göstermek için, görev kayıtlarınızı kendi BPM kitaplığınıza kaydetmelisiniz ve sonra Yardım sistemi parametrelerinizi BPM kitaplığınıza işaret edecek şekilde güncelleştirmelisiniz. Daha fazla bilgi için bkz. [Yardım sistemine bağlanma](../fin-and-ops/get-started/help-connect.md) Perakende Modern POS ve Bulut POS Yardımı, LCS'yi gerçek zamanlı olarak arar. Microsoft Dynamics 365 for Retail Yardım sistemi parametrelerinde seçili olan tüm BPM kütüphaneleri arasında arar ve ilgili sonuçları gösterir. **Yardım** menüsüne erişmek için ekranın üzerinde bulunan **Yardım** düğmesine (soru işareti) tıklayın ve daha sonra arama kutusu içerisinde işlem adınızı yazın ve ara düğmesine tıklayın. 

[![Yardım düğmesi](./media/help.jpg)](./media/help.jpg) 

Arama sonuçları içerisinde bir Görev kılavuzuna tıkladığınızda adımları bir Yardım konusu olarak görüntüleyebilir veya adımları bir Word belgesine aktarabilirsiniz. 
#### <a name="note"></a>Not
> Retail Modern POS ve Bulut POS'ta Yardım, hangi formda olduğunuza veya hangi işlemi yaptığınıza bağlı olarak görev kılavuzlarını getirmeyecektir. Arama kutusuna işlem adını yazıp **Ara** düğmesine tıklamanız gerekir.


