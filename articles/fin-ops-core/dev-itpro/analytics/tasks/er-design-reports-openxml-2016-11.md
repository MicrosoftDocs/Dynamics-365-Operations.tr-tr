---
title: ER OPENXML biçiminde raporlar oluşturmak için yapılandırma tasarlama (Kasım 2016)
description: Bu konuda, OPENXML biçiminde elektronik belgeler oluşturmak için bir şablon içeren yeni bir Elektronik raporlama yapılandırmasının nasıl oluşturulacağı açıklanmaktadır.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c3dfe6ce9c918b5fccbd7097096fa359facdf41bbf6fd0fab6c61153171484cd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753040"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>ER OPENXML biçiminde raporlar oluşturmak için yapılandırma tasarlama (Kasım 2016)

[!include [banner](../../includes/banner.md)]

Bu konuda Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının OPENXML biçiminde elektronik belgeler oluşturmak için bir şablon içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmaktadır. Bu yapılandırma, satıcı ödemelerini işlemek için kullanılacaktır.

Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, herhangi bir GBSI şirketinde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir. Ayrıca, şablonu oluştururken, alınacak olan bir Excel dosyası olmalıdır. Bu dosyaya [Ödeme Rapor Şablonu](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx)'ndan erişilebilir.


## <a name="upload-the-payments-data-model-configuration"></a>Ödemeler veri modeli konfigürasyonunu yükleme
1. Gezinti bölmesinde, **Modüller > Kuruluş yönetimi > Çalışma alanları > Elektronik raporlama**'ya gidin.
2. Listede, örnek şirket Litware, Inc. için yapılandırma sağlayıcısını işaretleyin. Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) bölümündeki adımları tamamlamalısınız.
3. **Etkin olarak ayarla**'ya tıklayın.
4. **Depolar**'ı seçin. Varsa, Operations Kaynakları türü için bir depo seçin. Kullanılabiliyorsa, yeni bir havuz oluşturmak hakkındaki aşağıdaki adımları atlayın.  
5. Açılır iletişim kutusunu açmak için **Ekle** öğesini seçin.
6. **Yapılandırma deposu türü** alanına `Operations resourcesdd` girin.
7. **Depo oluştur**'u seçin.
8. **Tamam**'ı seçin.
9. **Aç**'ı seçin.
10. Ağaçta, **Ödeme modeli**'ni seçin.
11. **İçe aktar**'ı seçin. Bu veri modelini içeri alın. Yeni bir biçim yapılandırılmasında veri kaynağı olarak kullanılır. Bu yapılandırmayı zaten içe aktardıysanız, bu adımı atlayın.  
12. **Evet**'i seçin.
13. Elektronik raporlama sayfasına dönene kadar sayfaları kapatın.

## <a name="create-a-new-format-configuration"></a>Yeni bir biçim yapılandırması oluşturma
1. **Raporlama yapılandırmaları**'nı seçin.
2. Ağaçta, **Ödeme modeli**'ni seçin.
3. Açılır iletişim kutusunu açmak için **Yapılandırma oluştur**'u seçin.
4. **Yeni** alanına `Format based on data model PaymentModel` girin. Bir biçimi, PaymentModel veri modeline dayalı olarak oluşturun.
5. **Ad** alanına `Sample worksheet report` yazın. Örnek çalışma sayfası raporu  
6. **Açıklama** alanına `Sample worksheet report for vendors' payments` yazın. Satıcıların ödemeleri için örnek çalışma sayfası raporu.  
7. **Veri modeli tanımı** alanına bir değer girin veya seçin. **CustomerCreditTransferInitiation** tanımını seçin.  
8. **Yapılandırma oluştur**'u seçin.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>OPENXML çalışma sayfası biçiminde yeni bir belge tasarlama
1. Ağaçta, **Ödeme modeli\Örnek çalışma sayfası raporu**'nu seçin.
2. **Tasarımcı**’yı seçin.
3. Eylem Bölmesinde, **İçe aktar**'ı seçin.
4. **Excel'den içe aktar**'ı seçin.
5. **Ekler**'i seçin. Şablon olarak mevcut Excel belgesini iliştirin.  
6. **Yeni**'yi seçin.
7. **Dosya**'yı seçin. Mevcut Excel dosyasına yönlendirin.  
8. Sayfayı kapatın.
9. **Şablon** alanına bir değer girin veya seçin. Şablon olarak kullanılmak üzere ekli Excel dosyasını seçin.  
10. **Tamam**'ı seçin. ER biçim bileşenlerinin, başvurulan MS Excel belgesinin (adlandırılmış aralıklar) yapısına dayalı bir tasarım biçiminde oluşturulduğunu unutmayın.  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Para birimi kodlarına göre toplamları hesaplamak için yeni bir veri kaynağı oluşturma
1. **Eşleme** sekmesini seçin.
2. Açılır iletişim kutusunu açmak için **Kök ekle**'yi seçin.
3. Ağaçta, **İşlevler\Gruplama ölçütü**'nü seçin.
4. **Ad** alanına `PaymentByCurrency` yazın.
5. **Grubu buna göre düzenle**'yi seçin.
6. Ağaçta, **model**'i genişletin, ardından **model\Ödemeler**'i seçin.
7. **Alanı buna ekle**'yi seçin.
8. **Neler gruplanacak**'ı seçin.
9. Ağaçta, **model\Ödemeler**'i genişletin, ardından **model\Ödemeler\Para birimi**'ni seçin.
10. **Alanı buna ekle**'yi seçin.
11. **Gruplandırılmış alanlar**'ı seçin.
12. Ağaçta, **model\Ödemeler\Talimat Tutarı(InstructedAmount)** seçeneğini belirleyin.
13. **Alanı buna ekle**'yi, ardından **Toplam alanları**'nı seçin.
14. **Yöntem** alanında bir seçenek belirleyin. **SUM toplama** işlevini seçin.  
15. **Ad** alanına `TotalInstructuredAmount` yazın.
16. **Kaydet**'i seçin.
17. Sayfayı kapatın.
18. **Tamam**'ı seçin.

## <a name="map-format-components-to-data-sources"></a>Biçim bileşenlerini veri kaynaklarına eşleme
1. Ağaçta, **model\Ödemeler\Başlatan Taraf(InitiatingParty)\Ad** ve **Excel\ReportHeader\CompanyName** seçeneğini belirleyin.
2. **Bağla**'yı seçin.
3. Ağaçta, **model\Ödemeler\Alacaklı\Kimlik\Kaynak Kimliği(SourceID)** ve **Excel\PaymLines\VendAccountName** seçeneğini belirleyin.
4. **Bağla**'yı seçin.
5. Ağaçta, **model\Ödemeler\Alacaklı\Ad** ve **Excel\PaymLines\VendName** seçeneğini belirleyin.
6. **Bağla**'yı seçin.
7. Ağaçta, **model\Ödemeler\Alacaklı Aracısı(CreditorAgent)\Ad** ve **Excel\PaymLines\Bank** seçeneğini belirleyin.
8. **Bağla**'yı seçin.
9. Ağaçta, **model\Ödemeler\Alacaklı Aracısı(CreditorAgent)\Rota Numarası(RoutingNumber)** ve **Excel\PaymLines\RoutingNumber** seçeneğini belirleyin.
10. **Bağla**'yı seçin.
11. Ağaçta, **model\Ödemeler\Alacaklı Hesabı(CreditorAccount)\Kimlik\Numara** ve **Excel\PaymLines\AccountNumber** seçeneğini belirleyin.
12. **Bağla**'yı seçin.
13. Ağaçta, **model\Ödemeler\Talimat Tutarı(InstructedAmount)** ve **Excel\PaymLines\Debit** seçeneğini belirleyin.
14. **Bağla**'yı seçin.
15. Ağaçta, **model\Ödemeler\Para Birimi** ve **Excel\PaymLines\Currency** seçeneğini belirleyin.
16. **Bağla**'yı seçin.
17. Ağaçta, **PaymentByCurrency\gruplanmış\Para Birimi** ve **Excel\SummaryLines\SummaryCurrency** seçeneğini belirleyin.
18. **Bağla**'yı seçin.
19. Ağaçta, **PaymentByCurrency\aggregated\TotalInstructuredAmount** ve **Excel\SummaryLines\SummaryAmount** seçeneğini belirleyin.
20. **Bağla**'yı seçin.
21. Ağaçta, **PaymentByCurrency** ve **Excel\SummaryLines** seçeneğini belirleyin.
22. **Bağla**'yı seçin.
23. Ağaçta, **model\Ödemeler** ve **Excel\PaymLines** seçeneğini belirleyin.
24. **Bağla**'yı seçin.
25. **Kaydet**'i seçip sayfayı kapatın.

## <a name="use-the-created-configuration-for-payments-processing"></a>Ödemeleri işlemek için oluşturulan yapılandırmayı kullanın
1. **Durumu değiştir**'i seçin.
2. **Tamamlandı**'yı seçin.
3. **Tamam**'ı seçin.
4. Gezinti bölmesinde, **Modüller > Borç hesapları > Ödeme ayarı > Ödeme yöntemleri**'ne gidin.
5. **Ödeme yöntemi** alanına **Elektronik** değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.
6. **Düzenle** öğesini seçin.
7. **Dosya biçimleri** bölümünü genişletin.
8. **Genel elektronik raporlama** alanında **Evet**'i seçin.
9. **Biçim yapılandırmasını dışa aktar** alanında bir değer girin veya seçin. **Örnek çalışma sayfası raporu** yapılandırmasını seçin.  
10. **Kaydet**'i seçin.
11. Sayfayı kapatın.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Oluşturulan yapılandırmayı ödeme günlüklerini işleme için kullanma
1. Gezinti bölmesinde **Modüller > Borç hesapları > Ödemeler > Ödeme günlüğü**'ne gidin.
2. Yeni bir ödeme günlüğü oluşturmak için **Yeni**'yi seçin.
3. **Ad** alanına **VendPay** yazın.
4. **Satırlar**'ı seçin.
5. **Hesap** alanında `GB_SI_000001` değerlerini belirtin.
6. **Borç** değerini `1000` olarak ayarlayın.
7. **Yeni**'yi seçin.
8. **Hesap** alanında `GB_SI_000005` değerlerini belirtin.
9. **Borç** değerini `2000` olarak ayarlayın.
10. **Para Birimi** alanına `EUR` yazın.
11. **Mahsup hesap** alanında `GBSI OPER` değerlerini belirtin.
12. **Ödeme yöntemi** alanına `Electronic` yazın.
13. **Kaydet**'i seçin.
14. **Ödemeleri oluştur**'u seçin.
15. **Ödeme yöntemi** alanına `Electronic` yazın.
16. **Dosya adı** alanına `Payments` yazın.
17. **Banka hesabı** alanına `GBSI OPER` yazın.
18. **Tamam**'ı, ardından yeniden **Tamam**'ı seçin. Oluşturulan çalışma sayfasını gözden geçirin; ödeme ayrıntı satırları ve bu ödeme iletisinde kullanılacak her bir para birimi kodu için toplamlar da dahil olmak üzere.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
