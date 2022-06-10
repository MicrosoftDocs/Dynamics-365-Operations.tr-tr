---
title: Kıymet yönetimi mobil çalışma alanını kullanma
description: Bu konu Varlık yönetimi mobil çalışma alanı hakkında bilgiler sağlar.
author: johanhoffmann
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 8b874237721d9252e7102c2611414a2cc74026c3
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811518"
---
# <a name="use-the-asset-management-mobile-workspace"></a>Kıymet yönetimi mobil çalışma alanını kullanma

[!include [banner](../../includes/banner.md)]
[!include [mobile app deprecated](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Bu konu **Kıymet yönetimi** mobil çalışma alanı hakkında bilgiler sağlar. Bu çalışma alanı, kullanıcıların bakım taleplerini ve iş emirlerini görüntüleyip oluşturmasına olanak tanır. Ayrıca kullanıcılar, atanan iş emri işlerini takvim veya liste görünümünde görüntüleyebilirler. Varlıklar ve işlem yapılacak yerleşimler de görüntülenip aranabilir.

## <a name="overview"></a>Genel bakış

Varlık Yönetimi, Dynamics 365 Supply Chain Management'da varlıkların ve iş emri işlerinin yönetilmesine yönelik gelişmiş bir modüldür. **Varlık yönetimi** mobil çalışma alanı, kullanıcıların istedikleri mobil cihazda atanan iş siparişi işlerini hızlı şekilde görüntülemesine olanak sağlar. Kullanıcılar ayrıca bakım talepleri oluşturabilir ve yönetebilir, yaşam döngüsü durumunu güncelleştirebilir ve varlık ve işlem yapılacak yerleşim ayrıntılarını mobil cihazlarını kullanarak görüntüleyebilir.

Özellikle, **Varlık yönetimi** mobil çalışma alanı, kullanıcıların şu görevleri yerine getirmesini sağlar:

- Bakım talepleri oluşturmak, görüntülemek ve düzenlemek, bir fotoğraf çekmek veya mevcut bir görüntüyü bakım talebine eklemek ve bakım talebi yaşam döngüsü durumunu değiştirmek. 
- İş emirleri oluşturmak, görüntülemek ve düzenlemek, bir fotoğraf çekmek veya mevcut bir görüntüyü iş emrine eklemek, iş emri yaşam döngüsü durumunu değiştirmek ve iş emri işlerini görüntülemek.
- Atanan iş emri işlerini Takvim görünümünde görüntülemek.
- İş emri işi oluşturmak, görüntülemek ve düzenlemek, varlık sayaçlarını güncelleştirmek, bakım denetim listesini görüntülemek, iş emri iş notlarını görüntülemek ve düzenlemek, iş emri işi için gerekli araçları görüntülemek.
- Belirli bir varlık veya işlem yapılacak yerleşimi görüntülemek veya aramak.

## <a name="prerequisites"></a>Önkoşullar

**Kıymet yönetimi** mobil çalışma alanını kullanabilmeniz için, yöneticinizin gerekli kullanıcı ve çalışan hesaplarını ayarlamış ve çalışma alanını yayımlamış olması gerekir. Daha fazla bilgi için bkz. [Kıymet yönetimi mobil çalışma alanını ayarlama](set-up-asset-management-mobile.md).

## <a name="download-and-install-the-mobile-app"></a>Mobil uygulamayı indirin ve yükleyin

Finance and Operations (Dynamics 365 ) mobil uygulamasını indirin ve yükleyin:

- [Android telefonlar için](https://go.microsoft.com/fwlink/?linkid=850662)
- [İPhone'lar için](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobil uygulamaya oturum açın

1. Mobil cihazınızda uygulamayı başlatın.

1. Dynamics 365 URL'nizi girin.

1. İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir. Kimlik bilgilerinizi girin.

1. Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir. Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.

    ![Çalışma alanını seçme.](media/am-mobile-01.png "Çalışma alanını seçme")

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a>Atanan iş emri işlerini Takvim görünümünde görüntüleme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

1. **İş emri işleri takvimim**'i seçin.

1. İş emri işlerini görüntülemek istediğiniz tarihi seçin. Listede, her iş emri işi için varlık kodunu ve işlem yapılacak yerleşim kodunu görürsünüz.

1. İş ayrıntılarını görmek için listeden bir iş emri işi seçin: Varlık ve işlem yapılacak yerleşim ayrıntıları ile **Ekler**, **Denetim listeleri**, **Araçlar**, **Varlık sayaçları**, **Notlar**, **Günlükler**'i görüntülemek için diğer gezinti bağlantıları.

    ![Atanan iş emri işlerini Takvim görünümünde görüntüleme.](media/am-mobile-02.png "Atanan iş emri işlerini Takvim görünümünde görüntüleme")

## <a name="create-a-work-order-job"></a>İş emri işi oluşturma

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

1. **Tüm bakım iş emirleri**'ni seçin.

1. Yeni bir iş emri işi oluşturmak istediğiniz iş emrini seçin.

1. **Satır ekle** düğmesini seçin.

1. Yeni bir iş emri işi oluşturmak istediğiniz **Varlığı** seçin.

1. **Bakım İşi türü**, **Bakım işi türü çeşidi** ve **Zanaat**'ı seçin.

1. **Tamam**'ı seçin.

    ![Satır ekle ekranı.](media/am-mobile-03.png "Satır ekle ekranı")


## <a name="add-attachment-to-a-work-order-job"></a>İş emri işine ek ekleme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

1. **Tüm bakım iş emirleri**'ni seçin.

1. Ek eklemek istediğiniz iş emrini > iş emri işini seçin.
    - Alternatif olarak, **İş emri işi ayrıntıları** sayfasına gitmek için ana sayfada **İş emri işleri listem** veya **İş emri işleri takvimim**'i seçebilirsiniz.

1. **İş emri işi ayrıntıları** sayfasında **Ekler**'i seçin.

1. İş emri işindeki mevcut ekleri göreceksiniz. **Ek ekle**'yi seçin.

1. Ek için **Ad** ve **Notlar** girin.

1. Mobil galeriden fotoğraf seçmek için **Görüntü seç**'i veya fotoğraf çekmek için **Fotoğraf çek**'i seçin.

1. **Tamam**'ı seçin.

    ![İş emri işi için ekleri görüntüleme ve ekleme.](media/am-mobile-04.png "İş emri işi için ekleri görüntüleme ve ekleme")

## <a name="view-maintenance-checklist-on-a-work-order-job"></a>İş emri işindeki bakım denetim listesini görüntüleme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

1. **Tüm bakım iş emirleri**'ni seçin.

1. Denetim listelerini görüntülemek istediğiniz iş emrini > iş emri işini seçin.
    - Alternatif olarak, **İş emri işi ayrıntıları** sayfasına gitmek için ana sayfada **İş emri işleri listem** veya **İş emri işleri takvimim**'i seçebilirsiniz.

1. **İş emri işi ayrıntıları** sayfasında **Denetim listeleri**'ni seçin.

1. İş emri işiyle ilgili denetim listesi satırlarının listesini göreceksiniz. **Yönergeleri** görüntülemek ve **Ekler** eklemek için denetim listesi satırı seçin.

1. Önceki sayfaya dönmek için geri düğmesini (**<**) seçin.

    ![Bakım denetim listesi ve satır ayrıntıları.](media/am-mobile-05.png "Bakım denetim listesi ve satır ayrıntıları")

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a>Bir iş emri işinde varlık sayaçlarını görüntüleme ve güncelleştirme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

1. **Tüm bakım iş emirleri**'ni seçin.

1. Varlık sayaçlarını görüntülemek istediğiniz iş emrini > iş emri işini seçin.
    - Alternatif olarak, **İş emri işi ayrıntıları** sayfasına gitmek için ana sayfada **İş emri işleri listem** veya **İş emri işleri takvimim**'i seçebilirsiniz.

1. **İş emri işi ayrıntıları** sayfasında **Varlık sayaçları**'nı seçin.

1. İş emri işiyle ilgili varlık sayaçlarının listesini göreceksiniz. Sayaç değerini güncelleştirmek için bir varlık sayacı satırındaki kalem simgesini seçin.

1. Yeni bir sayaç değeri girin ve **Bitti**'yi seçin.

    ![Kıymet sayaçlarını görüntüleme ve güncelleştirme.](media/am-mobile-06.png "Kıymet sayaçlarını görüntüleme ve güncelleştirme")

## <a name="register-consumption-on-a-work-order-job"></a>İş emri işinde tüketimi kaydetme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

1. **Tüm bakım iş emirleri**'ni seçin.

1. Tüketim kayıtları eklemek istediğiniz istediğiniz iş emrini > iş emri işini seçin.
    - Alternatif olarak, **İş emri işi ayrıntıları** sayfasına gitmek için ana sayfada **İş emri işleri listem** veya **İş emri işleri takvimim**'i seçebilirsiniz.

1. **İş emri işi ayrıntıları** sayfasında **Günlükler**'i seçin.

1. Çalışma saati kayıtları oluşturmak için **Saat ekle**'yi seçin.
    1. Aramadan **Kategori**'yi seçin.
    1. **Saat** alanında, iş emri işinde harcanan çalışma saatlerinin sayısını girin.
    1. Uygun **Satır özelliği** öğesini seçin.
    1. **Tamam**'ı seçin.

1. Madde kayıtları oluşturmak için **Madde ekle**'yi seçin.
    1. Aramadan **Madde numarası**'nı seçin.
    1. Aramadan **Tesis**'i seçin.
    1. Tüketilen madde **Miktarını** girin.
    1. **Tamam**'ı seçin.

1. Gider kayıtları oluşturmak için **Gider ekle**'yi seçin.
    1. Aramadan **Kategori**'yi seçin.
    1. Gider kaydı için miktarı girin.
    1. Aramadan **Satış para birimi**'ni seçin.
    1. Gider kaydı için **Maiyet fiyatı**'nı girin.
    1. **Tamam**'ı seçin.

    ![İş emri günlüğünü güncelleştirme.](media/am-mobile-07.png "İş emri günlüğünü güncelleştirme")

## <a name="update-lifecycle-state-on-a-work-order"></a>İş emrindeki yaşam döngüsü durumunu güncelleştirme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

1. **Tüm bakım iş emirleri**'ni seçin.

1. Yaşam döngüsü durumunu güncelleştirmek istediğiniz iş emrini seçin.

1. Ekranın alt kısmındaki **Durumu güncelleştir** düğmesini seçin.

1. Listeden yeni bir yaşam döngüsü durumu seçin.

1. **Tamam**'ı seçin.

    ![İş emrindeki yaşam döngüsü durumunu güncelleştirme.](media/am-mobile-08.png "İş emrindeki yaşam döngüsü durumunu güncelleştirme")

## <a name="create-a-maintenance-request"></a>Bakım talebi oluşturma

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

1. **Tüm bakım talepleri**'ni seçin.

1. Ekranın altınaki **Eylemler** öğesini ve **Bakım talebi oluştur**'u seçin.

1. **Varlık yönetimi**'nde bakım talepleri için numara serisi etkinleştirilmişse, **Bakım talebi** alanı gizlenir çünkü bu alan otomatik olarak doldurulur. **Bakım talebi** alanı görünüyorsa bir bakım talebi kimliği girin.

1. Bir **Bakım talebi türü** seçin.

1. Bakım talebi için bir **Açıklama** girin.

1. Talep oluşturmak istediğiniz **Varlığı** seçin.

1. Bakım talebi için **Hizmet düzeyi** seçin.

1. **Tamam**'ı seçin.

    ![Bakım talebi oluşturma.](media/am-mobile-09.png "Bakım talebi oluşturma")

## <a name="add-attachment-to-a-maintenance-request"></a>Bakım talebine ek ekleme

1. Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.

1. **Tüm bakım talepleri**'ni seçin.

1. Ek eklemek istediğiniz bakım talebini seçin.

1. Ekranın alt kısmındaki **Ekler**'i seçin.

1. **Ekler ekle**'yi seçin.

1. Ek için **Ad** ve **Notlar** girin.

1. Mobil galeriden fotoğraf seçmek için **Resim seç**'i veya fotoğraf çekmek için **Fotoğraf çek**'i seçin.

1. **Tamam**'ı seçin.

    ![Bakım talebine ek ekleme.](media/am-mobile-10.png "Bakım talebine ek ekleme")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
