---
title: Yan hak bildirimi
description: Yan hak bildirimi raporu, çalışanın şu anda kayıtlı olduğu kazançları açıklar.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a12649cd0604fb6acd58420fdafb5b560fcc10cf
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688246"
---
# <a name="benefit-statement"></a>Yan hak bildirimi


[!INCLUDE [PEAP](../includes/peap-2.md)]

**Yan hak bildirimi** raporu, çalışanın şu anda kayıtlı olduğu avantajların açıklamasını sağlar. Rapora, doğrudan bir çalışan veya kazanç yöneticisi tarafından erişilebilir. **Yan hak bildirimi**; çalışanın kayıtlı kazançları, karşılama seçenekleri, maliyetleri, kayıtlı bağımlıları veya lehdarlarının listesini sağlar. Bildirim, tek bir çalışan veya birden çok çalışan için yazdırılabilir.

> [!NOTE]
**Yan hak bildirimi** özelliği, **Özellik yönetimi** çalışma alanında etkinleştirilmelidir. Bunu yapmak için Özellik yönetiminde **Yan hak yönetimi** özelliğinin açılması gerekir. 


## <a name="importing-the-benefit-statement"></a>Yan hak bildirimini içeri aktarma 

**Yan hak bildirimi**'nin kullanılabilir olması için rapor yapılandırmasını kullanarak **Yan hak bildirimi**'ni içeri aktarmanız gerekir. Bunu yapmak için aşağıdaki adımları tamamlayın:

1.  **Sistem Yönetimi** çalışma alanına gidin.

2.  **Elektronik Raporlama** kutucuğunu seçin.

3.  **Yapılandırma sağlayıcıları**'na gidin ve **Depolar**'ı seçin.

  ![Depolar seçimi.](https://user-images.githubusercontent.com/26801678/134203290-7faf7245-ed08-44e9-95a1-a7ba278c42c6.png)

4.  **İK kaynakları**'nı seçin ve ardından **Aç** seçeneğini belirleyin.

    ![Konfigürasyon havuzları.](https://user-images.githubusercontent.com/26801678/134203619-b3fd087d-1fe9-45ef-a588-1afedfe38dfd.png)

5.  Sol bölmede **Yan hak bildirimi modeli**'ni seçin ve **Yan hak bildirimi biçimi** görüntülenecek şekilde genişletin.

6.  Sol bölmede **Yan hak bildirimi biçimi**'ni seçin.

7.  Ekranın sağ tarafında, **Sürümler** hızlı sekmesi bulunur. **İçe aktar**'ı seçin.

    ![Sürümler hızlı sekmesi.](https://user-images.githubusercontent.com/26801678/134203763-f12ef549-e326-400d-ac69-b25fc94af47b.png)

## <a name="generate-the-benefit-statement-as-a-pdf-file"></a>Yan hak bildirimini PDF Dosyası olarak oluşturma

Varsayılan olarak **Yan hak bildirimi**, Microsoft Word belgesi olarak yazdırılır. PDF biçiminde yazdırmak için **Elektronik raporlama hedefi**'nde PDF seçeneğini yapılandırmanız gerekir. 

1. Bunu yapmak için **Sistem yönetimi çalışma alanı** > **Elektronik raporlama** > **İlgili bağlantılar** > **Elektronik raporlama hedefi**'ne gidin.

1.  **Yeni**'yi seçin.

2.  **Referans** alanında, **Yan hak bildirimi biçimi**'ni seçin.

3.  **Dosya hedefi** hızlı sekmesinde **Yeni**'yi seçin.

4.  **Ad** alanına **Yan Hak Bildirimi PDF'si** ifadesini girin.

5.  **Dosya bileşeni adı** alanında **Yan hak bildirimi**'ni seçin.

6.  **PDF'ye dönüştür** onay kutusunu seçin.

7.  Menü öğesinden **Ayarlar**'ı seçin. 

    ![Dosya hedefi.](https://user-images.githubusercontent.com/26801678/134203881-a3f1ebc3-d816-485d-a53b-026cc29cae64.png)

8.  **Dosya** hızlı sekmesini seçin ve ardından **Etkin** seçeneğini belirleyin.

9.  **Tamam**'ı seçin.
   
> [!NOTE]
> Kazanç yönetimi özelliği, Önizleme durumundadır. **Elektronik raporlama hedefi** raporunda e-posta hedefi ayarı kullanılırken bilinen bir sorun oluşur. Hata iletisi alabilirsiniz ve e-posta gönderilemez.

**Yan hak bildirimi** aşağıdaki sayfalardan oluşturulabilir:

-   **Kazanç yönetimi çalışma alanı** > **Bağlantılar** > **Raporlar** > **Yan hak bildirimi**

-   **Çalışanlar (eski form)** > **Kişisel bilgiler sekmesi** > **Yan hak bildirimi**

-   **Kolaylaştırılmış personel girişi** > **Kazanç raporları** > **Yan hak bildirimi**

-   **Personel self servisi** > **Kazançlar** > **Yan hak bildirimini görüntüle**

> [!NOTE]
>  **Personel self servisi**'nde **Yan hak bildirimi**'ne erişim, **Yan hak bildirimini görüntüle** ayrıcalığı tarafından denetlenir. Bu, **Personel Self Servisi Kazançları** görevi altındadır. Bu ayrıcalık, varsayılan olarak çalışanlara verilir.

## <a name="report-contents"></a>Rapor içeriği

**Yan hak bildirimi**'nde, feragat edilen planlar dahil olmak üzere çalışanın onaylı plan seçimleri yazdırılır. Aşağıdaki görüntüde bu raporun bir örneği gösterilmektedir. 

![Yan hak bildirimi raporu.](https://user-images.githubusercontent.com/26801678/134204058-61baa318-fede-4795-a256-acdf3217f9f9.png)

Raporda **Plan**, **Karşılama seçeneği**, **Personel maliyeti** ve **İşveren maliyeti** görüntülenir. Raporda ayrıca kapsanan bağımlılar da listelenir. Planda bununla ilişkili lehdarlar varsa lehdarlar ve dağıtım öncelikleri ve yüzdeleri görüntülenir.

**Yan hak bildirimi** raporu, **Yan hak bildirimi** sayfasında **Eklenecek kayıtlar** hızlı sayfasını kullanarak aynı anda birden çok kullanıcı için yazdırılabilir.
