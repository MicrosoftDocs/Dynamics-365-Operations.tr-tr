--- 
title: "Biçim çıktılarında Belge Yönetimi dosyalarını kullanmak için biçim çalıştırma"
description: "Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 554de60fb8d2b6cb03cac5dc8d01df98390ad844
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="run-format-to-use-document-management-files-in-format-outputs"></a>Biçim çıktılarında Belge Yönetimi dosyalarını kullanmak için biçim çalıştırma 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar. Bu adımlar DEMF şirketinde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 3: Biçimi çalıştırma)" yordamındaki adımları tamamlamalısınız.

Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Tek bir faturanın satış siparişi için gerekli ekleri ekleyin
1. Alacak hesapları > Faturalar > Açık müşteri faturaları'na gidin.
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, "CIV-000148" değerine sahip Fatura alanı üzerinde filtreleme uygulayın.
    * CIV-000148  
3. Seçilen faturanın bağlantısını izlemek için tıklayın.
    * CIV-000148  
4. Satış siparişi alanındaki bağlantıyı izlemek için tıklayın.
    * 000148  
5. Satırlar veya başlık alanında Başlık seçeneğini belirleyin.
    * Ekleri eklemek için hedef olacağını belirtmek için Başlığı seçin.  
6. İliştir'e tıklayın.
    * Bu satış siparişi için ek olarak birkaç dosya ekleyin. Belge Yönetimi tarafından desteklenen belge türlerinden dosyaları kullanın (DOCX, DPF, XML, JPG, vb. dosya uzantıları). Eklenecek ve ER elektronik iletisinde faturayla ilgili olarak işlenecek dosyalara göz atın ve seçin.  
7. Yeni'ye tıklayın.
8. Dosya'ya tıklayın.
9. Yeni'ye tıklayın.
10. Dosya'ya tıklayın.
11. Sayfayı kapatın.
12. Sayfayı kapatın.
13. Sayfayı kapatın.
14. Sayfayı kapatın.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Seçili fatura için tasarlanan raporu çalıştırın
1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.
3. Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)"i genişletin.
4. Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)\Elektronik fatura örnek iletisi"ni seçin.
5. Çalıştır öğesine tıklayın.
6. Eklenecek kayıtlar () bölümünü genişletin.
7. Filtre'ye tıklayın.
8. Müşteri fatura günlüğü satırını ve Satış siparişi alanını seçin.
9. Ölçütler alanına '000148' yazın.
    * "Satış siparişi" ölçütler alanında sipariş numarası olarak 000148 yazın.  
10. Tamam'a tıklayın.
11. Tamam'a tıklayın.
    * Ortaya çıkan sonucu inceleyin. Her ek için tek bir XML düğümü oluşturulduğunu unutmayın. Ek'in içeriği XML çıktısına MIME (base64) metin biçiminde doldurulur.  


