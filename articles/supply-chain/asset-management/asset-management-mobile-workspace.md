---
title: Varlık yönetimi mobil çalışma alanı
description: Bu konu Varlık yönetimi mobil çalışma alanı hakkında bilgiler sağlar.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: fd6f45a7dc9d062a3602499e89a6473b3b4aeaee
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278405"
---
# <a name="asset-management-mobile-workspace"></a>Varlık yönetimi mobil çalışma alanı

[!include [banner](../../includes/banner.md)]


Bu konu Varlık yönetimi mobil çalışma alanı hakkında bilgiler sağlar. Bu çalışma alanı, kullanıcıların bakım taleplerini ve iş emirlerini görüntüleyip oluşturmasına olanak tanır. Ayrıca kullanıcılar, atanan iş emri işlerini takvim veya liste görünümünde görüntüleyebilirler. Varlıklar ve işlem yapılacak yerleşimler de görüntülenip aranabilir.


## <a name="overview"></a>Genel bakış

Varlık Yönetimi, Dynamics 365 Supply Chain Management'da varlıkların ve iş emri işlerinin yönetilmesine yönelik gelişmiş bir modüldür. **Varlık yönetimi** mobil çalışma alanı, kullanıcıların istedikleri mobil cihazda atanan iş siparişi işlerini hızlı şekilde görüntülemesine olanak sağlar. Kullanıcılar ayrıca bakım talepleri oluşturabilir ve yönetebilir, yaşam döngüsü durumunu güncelleştirebilir ve varlık ve işlem yapılacak yerleşim ayrıntılarını mobil cihazlarını kullanarak görüntüleyebilir.

Özellikle, **Varlık yönetimi** mobil çalışma alanı, kullanıcıların şu görevleri yerine getirmesini sağlar:

- Bakım talepleri oluşturmak, görüntülemek ve düzenlemek, bir fotoğraf çekmek veya mevcut bir görüntüyü bakım talebine eklemek ve bakım talebi yaşam döngüsü durumunu değiştirmek. 
- İş emirleri oluşturmak, görüntülemek ve düzenlemek, bir fotoğraf çekmek veya mevcut bir görüntüyü iş emrine eklemek, iş emri yaşam döngüsü durumunu değiştirmek ve iş emri işlerini görüntülemek.
- Atanan iş emri işlerini Takvim görünümünde görüntülemek.
- İş emri işi oluşturmak, görüntülemek ve düzenlemek, varlık sayaçlarını güncelleştirmek, bakım denetim listesini görüntülemek, iş emri iş notlarını görüntülemek ve düzenlemek, iş emri işi için gerekli araçları görüntülemek.
- Belirli bir varlık veya işlem yapılacak yerleşimi görüntülemek veya aramak.


## <a name="prerequisites"></a>Önkoşullar

Önkoşullar, kuruluşunuza dağıtılan Dynamics 365 Supply Chain Management sürümüne dayalı olarak değişiklik gösterir.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-supply-chain-management"></a>Microsoft Dynamics 365 Supply Chain Management kullanıyorsanız önkoşullar 
Microsoft Dynamics 365 Supply Chain Management kuruluşunuza dağıtıldıysa sistem yöneticisinin **Varlık yönetimi** mobil çalışma alanını yayımlaması gerekir. Yönergeler için bkz: [Bir mobil çalışma alanı yayımlama](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

## <a name="download-and-install-the-mobile-app"></a>Mobil uygulamayı indirin ve yükleyin
Dynamics 365 for Unified Operations mobil uygulamasını yükleyin ve kurun:

- [Android telefonlar için](https://go.microsoft.com/fwlink/?linkid=850662)
- [İPhone'lar için](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobil uygulamaya oturum açın
1. Mobil cihazınızda uygulamayı başlatın.

2. Dynamics 365 URL'nizi girin.

3. İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir. Kimlik bilgilerinizi girin.

4. Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir. Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.

![Şekil 1](media/am-mobile-01.png)


## <a name="view-assigned-work-order-jobs-in-calendar-view"></a>Atanan iş emri işlerini Takvim görünümünde görüntüleme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

2. **İş emri işleri takvimim**'i seçin.

3. İş emri işlerini görüntülemek istediğiniz tarihi seçin. Listede, her iş emri işi için varlık kodunu ve işlem yapılacak yerleşim kodunu görürsünüz.

4. İş ayrıntılarını görmek için listeden bir iş emri işi seçin: Varlık ve işlem yapılacak yerleşim ayrıntıları ile **Ekler**, **Denetim listeleri**, **Araçlar**, **Varlık sayaçları**, **Notlar**, **Günlükler**'i görüntülemek için diğer gezinti bağlantıları.

![Şekil 2](media/am-mobile-02.png)


## <a name="create-a-work-order-job"></a>İş emri işi oluşturma

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

2. **Tüm bakım iş emirleri**'ni seçin.

3. Yeni bir iş emri işi oluşturmak istediğiniz iş emrini seçin.

4. **Satır ekle** düğmesini seçin.

5. Yeni bir iş emri işi oluşturmak istediğiniz **Varlığı** seçin.

6. **Bakım İşi türü**, **Bakım işi türü çeşidi** ve **Zanaat**'ı seçin.

7. **Tamam**'ı seçin.

![Şekil 3](media/am-mobile-03.png)


## <a name="add-attachment-to-a-work-order-job"></a>İş emri işine ek ekleme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

2. **Tüm bakım iş emirleri**'ni seçin.

3. Ek eklemek istediğiniz iş emrini > iş emri işini seçin.
    - Alternatif olarak, **İş emri işi ayrıntıları** sayfasına gitmek için ana sayfada **İş emri işleri listem** veya **İş emri işleri takvimim**'i seçebilirsiniz.

4. **İş emri işi ayrıntıları** sayfasında **Ekler**'i seçin.

5. İş emri işindeki mevcut ekleri göreceksiniz. **Ek ekle**'yi seçin.

6. Ek için **Ad** ve **Notlar** girin.

7. Mobil galeriden fotoğraf seçmek için **Görüntü seç**'i veya fotoğraf çekmek için **Fotoğraf çek**'i seçin.

8. **Tamam**'ı seçin.

![Şekil 4](media/am-mobile-04.png)


## <a name="view-maintenance-checklist-on-a-work-order-job"></a>İş emri işindeki bakım denetim listesini görüntüleme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

2. **Tüm bakım iş emirleri**'ni seçin.

3. Denetim listelerini görüntülemek istediğiniz iş emrini > iş emri işini seçin.
    - Alternatif olarak, **İş emri işi ayrıntıları** sayfasına gitmek için ana sayfada **İş emri işleri listem** veya **İş emri işleri takvimim**'i seçebilirsiniz.

4. **İş emri işi ayrıntıları** sayfasında **Denetim listeleri**'ni seçin.

5. İş emri işiyle ilgili denetim listesi satırlarının listesini göreceksiniz. **Yönergeleri** görüntülemek ve **Ekler** eklemek için denetim listesi satırı seçin.

6. Önceki sayfaya dönmek için geri düğmesini (**<**) seçin.

![Şekil 5](media/am-mobile-05.png)


## <a name="view-and-update-asset-counters-on-a-work-order-job"></a>Bir iş emri işinde varlık sayaçlarını görüntüleme ve güncelleştirme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

2. **Tüm bakım iş emirleri**'ni seçin.

3. Varlık sayaçlarını görüntülemek istediğiniz iş emrini > iş emri işini seçin.
    - Alternatif olarak, **İş emri işi ayrıntıları** sayfasına gitmek için ana sayfada **İş emri işleri listem** veya **İş emri işleri takvimim**'i seçebilirsiniz.

4. **İş emri işi ayrıntıları** sayfasında **Varlık sayaçları**'nı seçin.

5. İş emri işiyle ilgili varlık sayaçlarının listesini göreceksiniz. Sayaç değerini güncelleştirmek için bir varlık sayacı satırındaki kalem simgesini seçin.

6. Yeni bir sayaç değeri girin ve **Bitti**'yi seçin.

![Şekil 6](media/am-mobile-06.png)


## <a name="register-consumption-on-a-work-order-job"></a>İş emri işinde tüketimi kaydetme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

2. **Tüm bakım iş emirleri**'ni seçin.

3. Tüketim kayıtları eklemek istediğiniz istediğiniz iş emrini > iş emri işini seçin.
    - Alternatif olarak, **İş emri işi ayrıntıları** sayfasına gitmek için ana sayfada **İş emri işleri listem** veya **İş emri işleri takvimim**'i seçebilirsiniz.

4. **İş emri işi ayrıntıları** sayfasında **Günlükler**'i seçin.

5. Çalışma saati kayıtları oluşturmak için **Saat ekle**'yi seçin.
    1. Aramadan **Kategori**'yi seçin.
    2. **Saat** alanında, iş emri işinde harcanan çalışma saatlerinin sayısını girin.
    3. Uygun **Satır özelliği** öğesini seçin.
    4. **Tamam**'ı seçin.

6. Madde kayıtları oluşturmak için **Madde ekle**'yi seçin.
    1. Aramadan **Madde numarası**'nı seçin.
    2. Aramadan **Tesis**'i seçin.
    3. Tüketilen madde **Miktarını** girin.
    4. **Tamam**'ı seçin.

7. Gider kayıtları oluşturmak için **Gider ekle**'yi seçin.
    1. Aramadan **Kategori**'yi seçin.
    2. Gider kaydı için miktarı girin.
    3. Aramadan **Satış para birimi**'ni seçin.
    4. Gider kaydı için **Maiyet fiyatı**'nı girin.
    5. **Tamam**'ı seçin.

![Şekil 7](media/am-mobile-07.png)


## <a name="update-lifecycle-state-on-a-work-order"></a>İş emrindeki yaşam döngüsü durumunu güncelleştirme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

2. **Tüm bakım iş emirleri**'ni seçin.

3. Yaşam döngüsü durumunu güncelleştirmek istediğiniz iş emrini seçin.

4. Ekranın alt kısmındaki **Durumu güncelleştir** düğmesini seçin.

5. Listeden yeni bir yaşam döngüsü durumu seçin.

6. **Tamam**'ı seçin.

![Şekil 8](media/am-mobile-08.png)


## <a name="create-a-maintenance-request"></a>Bakım talebi oluşturma

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

2. **Tüm bakım talepleri**'ni seçin.

3. Ekranın altınaki **Eylemler** öğesini ve **Bakım talebi oluştur**'u seçin.

4. **Varlık yönetimi**'nde bakım talepleri için numara serisi etkinleştirilmişse, **Bakım talebi** alanı gizlenir çünkü bu alan otomatik olarak doldurulur. **Bakım talebi** alanı görünüyorsa bir bakım talebi kimliği girin.

5. Bir **Bakım talebi türü** seçin.

6. Bakım talebi için bir **Açıklama** girin.

7. Talep oluşturmak istediğiniz **Varlığı** seçin.

8. Bakım talebi için **Hizmet düzeyi** seçin.

9. **Tamam**'ı seçin.

![Şekil 9](media/am-mobile-09.png)


## <a name="add-attachment-to-a-maintenance-request"></a>Bakım talebine ek ekleme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

2. **Tüm bakım talepleri**'ni seçin.

3. Ek eklemek istediğiniz bakım talebini seçin.

4. Ekranın alt kısmındaki **Ekler**'i seçin.

5. **Ekler ekle**'yi seçin.

6. Ek için **Ad** ve **Notlar** girin.

7. Mobil galeriden fotoğraf seçmek için **Görüntü seç**'i veya fotoğraf çekmek için **Fotoğraf çek**'i seçin.

8. **Tamam**'ı seçin.

![Şekil 10](media/am-mobile-10.png)

