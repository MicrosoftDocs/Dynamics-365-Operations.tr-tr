--- 
title: "Elektronik raporlama (ER) için bir Microsoft Excel şablonunu yeniden uygulayarak biçimi değiştirme"
description: "Bu yordamdaki bu adımı tamamlamak için öncelikle \"OPENXML biçiminde raporlar oluşturmak için bir ER yapılandırması tasarlama\" yordamındaki adımları tamamlamanız gerekir."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: b49cfe39732a450e4723419c50d8bcc3d64b7ec9
ms.openlocfilehash: 2f35727376812b0de428ce929ebe0d33bc497984
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="modify-a-format-by-reapplying-a-microsoft-excel-template-for-electronic-reporting-er"></a>Elektronik raporlama (ER) için bir Microsoft Excel şablonunu yeniden uygulayarak biçimi değiştirme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordamdaki bu adımı tamamlamak için öncelikle "OPENXML biçiminde raporlar oluşturmak için bir ER yapılandırması tasarlama" yordamındaki adımları tamamlamanız gerekir.

Bu yordam, değiştirilmiş bir Microsoft Excel şablonu kullanarak bir Elektronik raporlama (ER) biçim yapılandırmasını nasıl değiştireceğinizi açıklar. Bu yordamda, değiştirilmiş bir Excel şablonunu, aynı şirket Litware, Inc. için oluşturulmuş bir ER biçim yapılandırmasına içe aktaracak ve daha sonra elektronik belgeler oluşturacaksınız. Bu yordam sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne sahip kullanıcılar içindir. Bu adımlar GBSI veri kümesi kullanılarak tamamlanabilir. Başlamadan önce, Elektronik raporlama biçimini bir Excel şablonunu yeniden uygulayarak değiştir Yardım konusu içerisinde listelenen SampleVendPaymWsReport2.xlsx dosyasını indirin ve kaydedin (modify-electronic-reporting-format-reapply-excel-template/).

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlayın.  

## <a name="select-the-er-format"></a>ER biçimini seçin
1. Raporlama konfigürasyonları'na tıklayın.
2. Ağaçta, 'Ödeme modeli' öğesini genişletin.
3. Ağaçta, 'Ödeme modeli\Örnek çalışma sayfası raporu' seçin.
4. Ekler'e tıklayın.
    * SampleVendPaymWsReport.xlsx Excel dosyasının şu an ödeme günlüğü işlem için bir şablon olarak kullanıldığını unutmayın.   
5. Aç'a tıklayın.
    * Excel şablonunun düzenini keşfetmek için Aç'ı tıklatın.  
    * Şablonu gözden geçirin. Mevcut olarak her bir ödeme satırı için aşağıdaki ayrıntıları içerdiğini unutmayın: satıcı hesap numarası, satıcı adı, banka rota numarası, hesap numarası, borç, alacak ve para birimi. Bu örnek için bu listeyi ödeme tarihi hakkında ayrıntılar girerek genişletmek istiyoruz.   
6. Sayfayı kapatın.

## <a name="reapply-a-new-excel-template-to-er-format"></a>ER biçimine yeni bir Excel şablonunu yeniden uygulayın
1. Tasarımcı'yı tıklatın.
    * Düzenlemek için seçilen ER biçiminin taslak sürümünü açın.  
2. Eylem Bölmesinde, İçeri Al'a tıklayın.
3. Excel'den güncelleştir'e tıklayın.
    * 'Şablonu güncelleştir' üzerine tıklayın ve daha sonra SampleVendPaymWsReport2.xlsx dosyasını seçin.  
    * Daha önce indirilen SampleVendPaymWsReport2.xlsx dosyasına erişmek için Şablonu güncelleştir ve göz at üzerine tıklayın.  
4. Tamam'a tıklayın.
    * The SampleVendPaymWsReport2.xlsx şablonu uygulanır. ER biçiminin yapısı, öğeleri ER biçimine aktarılan şablonun içeriğiyle eşleştirilir. ER biçimindeki şablona eklenmeyen tüm mevcut öğeler biçim tanımından çıkartılır.  
5. Ağaçta, 'Excel' metnini seçin.
    * Şablon alanının şimdi yeni şablona bir referans içerdiğini dikkate alın.   
6. Ekler'e tıklayın.
7. Aç'a tıklayın.
    * Değiştirilen Excel şablonunun düzenini keşfetmek için Aç'ı tıklatın.  
    * Şablonu gözden geçirin. Şimdi ödeme tarihi için bir satır içerdiğini dikkate alın.   
8. Sayfayı kapatın.
9. Ağaçta, 'Excel' metnini genişletin.
10. Ağaçta, "Excel\PaymLines" öğesini genişletin.
11. Ağaçta 'Excel\PaymLines\PaymDate' seçin.
    * ER biçiminin şimdi bir öğe daha içerdiğini unutmayın. Bir hücre, PaymDate şimdi Excel şablonuna eklenmiştir.  
12. Eşleme sekmesini tıklatın.
13. Ağaçta, 'model'i genişletin.
14. Ağaçta genişletin 'model\Payments'.
15. Ağaçta seçin 'model\Payments\Transaction date(TransactionDate)'.
16. Bağla'ya tıklayın.
    * Hangi verinin çalışma zamanında yeni hücreye ekleneceğini belirtin.  
17. Kaydet'e tıklayın.
18. Sayfayı kapatın.

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>ER biçiminin değiştirilmiş taslak sürümünü, ödeme günlüğü işlemede kullanmak için etkinleştirin
1. Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.
2. Kullanıcı parametreleri'ne tıklayın.
3. Çalıştırma ayarları alanında Evet'i seçin.
4. Tamam'a tıklayın.
5. Düzenle öğesine tıklayın.
6. Taslak Çalıştır alanında Evet'e tıklayın.

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>ER biçiminin değiştirilmiş taslak sürümünü, ödeme günlüğü işlemede kullanın
    * Yeni ödeme satırlarının - ödeme tarihinin ayrıntıları da dahil oluşturulan çalışma sayfasını gözden geçirin.  


