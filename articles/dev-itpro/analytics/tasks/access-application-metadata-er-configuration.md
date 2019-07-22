---
title: ER yapılandırma kullanarak uygulama meta verilerine erişim
description: Bu konudaki adımlarda, Regulatory Configuration Service (RCS) kullanıcısının, Finance and Operations'ta meta verileri kullanarak yeni bir elektronik raporlama (ER) modeli eşlemesi tasarlayabileceği açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b95b41b27cecd4c71ed7646f329cf5736a01b561
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727041"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>ER yapılandırma kullanarak uygulama meta verilerine erişim

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama rolüne sahip Regulatory Configuration Service (RCS) kullanıcısının Dynamics 365 for Finance and Operations uygulamasının meta verilerini kullanarak nasıl yeni bir Elektronik raporlama (ER) modeli eşlemesi tasarlayabildiğini açıklar. Uygulama meta verilerine, dış ticari hareketlere erişmek için örnek bir meta veri kümesi içeren ER meta veri yapılandırması kullanılarak erişilir. RCS'de bu adımları tamamlamak için ilk olarak, [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları tamamlamanız gerekir. Daha sonra Finance and Operations konsundaki adımları tamamlayın, [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).

## <a name="prerequisites"></a>Önkoşullar
1. **Tüm çalışma alanları** > **Elektronik raporlama**'ya gidin. 
2. Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız[Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md). prosedüründeki adımları tamamlayın. 

## <a name="import-metadata-configuration"></a>Meta veri yapılandırmasını içe aktarın 
1. **Meta veri yapılandırması**'na tıklayın. 
2. Dış ticaret işletmesine elektronik belge oluşturmak üzere yapılandırılmış olan Finance and Operations uygulamasından meta veriler içeren ER meta veri yapılandırmasını içe aktarın. Bu ER meta veri yapılandırması [(ER) RCS'de kullanılacak uygulama meta verileri hazırlama](prepare-application-metadata-rcs.md) adımı tamamlandığında XML dosyası olarak dışa aktarılır. 
3. **Değiştir**'e tıklayın. 
4. **XML dosyasından yükle**'ye tıklayın. 
5. **Gözat**'a tıklayın ve "Dış ticaret meta verileri.xml" dosyasını seçin. 
6. **Tamam**'a tıklayın. 
7. Sayfayı kapatın. 

## <a name="create-data-model-configuration"></a>Veri modeli yapılandırması oluşturun
1. **Raporlama konfigürasyonları**'na tıklayın. 
2. İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın. 
3. **Ad** alanına, "Dış ticaret modeli" yazın. 
4. **Konfigürasyon oluştur**'u tıklatın. 
5. **Tasarımcı**'yı tıklatın. 
6. Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın. 
7. **Ad** alanına "Kök" yazın. 
8. **Ekle** öğesine tıklayın. 
9. Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın. 
10. **Ad** alanına "Hareket" yazın. 
11. **Madde türü** alanında **Kayıt listesi**'ni seçin. 
12. **Ekle** öğesine tıklayın. 
13. Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın. 
14. **Ad** alanına "Emtia kodu" yazın. 
15. **Madde türü** alanında **Dize**'yi seçin. 
16. **Ekle** öğesine tıklayın. 
17. Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın. 
18. **Ad** alanına "Faturalanan tutar" yazın. 
19. **Madde türü** alanında **Gerçek**'i seçin. 
20. **Ekle** öğesine tıklayın. 
21. Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın. 
22. **Ad** alanına "Tarih" yazın. 
23. **Madde türü** alanında **Tarih**'i seçin. 
24. **Ekle** öğesine tıklayın. 
25. **Kök referansı**'na tıklayın. 
26. **Tamam**'a tıklayın. 
27. **Kaydet**'e tıklayın. 
28. Sayfayı kapatın. 
29. **Durumu değiştir** öğesine tıklayın. 
30. **Tamamla** öğesine tıklayın. 
31. **Tamam**'a tıklayın. 

## <a name="create-model-mapping-configuration"></a>Model eşleme yapılandırma oluşturma 
1. İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın. 
2. **Yeni** alanına, "Dış ticaret modeli veri modelini temel alan Model Eşleme" yazın. 
3. **Ad** alanına, "Dış ticaret eşlemesi" yazın. 
4. **Konfigürasyon oluştur**'u tıklatın. 
5. **Önkoşullar** bölümünü genişletin. 
6. **Düzenle**'yi tıklatın. 
7. **Yeni**'ye tıklayın. 
8. Listede, seçili satırı işaretleyin. 
9. **Önkoşul bileşen türü** alanında **Yapılandırma**'yı seçin. 
10. **Dış ticaret meta veri** yapılandırılması seçin. 
11. **Kaydet**'e tıklayın. 
12. "Dış ticaret meta verileri" yapılandırmasındaki sürüm 1' e referans ekledik. Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verileri sunulacaktır. 
13. Sayfayı kapatın. 
14. **Tasarımcı**'yı tıklatın. 
15. **Tasarımcı**'yı tıklatın. 
16. Ağaçta, **Dynamics 365 for Operations\Tablo kayıtları**'nı seçin. 
17. **Kök ekle**'ye tıklayın. 
18. **Ad** alanına "Intrastat" yazın. 
19. **Intrastat** tablosu kayıtlarını seçin. 
20. **Tamam**'a tıklayın. 

> [!NOTE]
> Şu anda kullanılmakta olan meta veri kümesine sadece 2 tablo eklendiğinden sadece 2 tablo sunuldu. 

21. **Bağla**'ya tıklayın. 
22. Ağaçta **Intrastat**'ı genişletin. 
23. Ağaçta **Intrastat\AmountMST**'yi seçin. 
24. Ağaçta **Hareket = Intrastat**'ı genişletin. 
25. Ağaçta **Hareket = Intrastat\Faturalanan tutar**'ı seçin. 
26. **Bağla**'ya tıklayın. 
27. Ağaçta **Intrastat\TransDate**'i seçin. 
28. Ağaçta **Hareket = Intrastat\Tarih**'i seçin. 
29. **Bağla**'ya tıklayın. 
30. Ağaçta **Intrastat\>İlişkiler**'i genişletin. 
31. Ağaçta **Intrastat\>İlişkiler\IntrastatCommodity**'i genişletin. 
32. Ağaçta **Intrastat\>İlişkiler\IntrastatCommodity\Code**'u seçin. 
33. Ağaçta **Hareket = Intrastat\Emtia kodu**'nu seçin. 
34. **Bağla**'ya tıklayın. 
35. **Doğrula**'ya tıklayın. 

> [!NOTE]
> Belirtilen veri kaynağı öğeleriyle, başvurulan ER meta veri yapılandırmasından uygulama meta verilerinin ayrıntılarını kullanarak tanımlanan veri modeli öğelerini başarıyla bağladık. 
36. **Kaydet**'e tıklayın. 
37. Sayfayı kapatın. 
38. Sayfayı kapatın. 
39. Varolan meta veri kümesini genişletmeniz gerektiğinde bunu Finance and Operations'tan yapabilirsiniz. Sonra acil durumda kurtarma için meta veri yapılandırmasının yeni sürümünü Finance and Operations'tan içe aktarabilir, bunları RCS 'ye aktarabilir ve alınan meta veri yapılandırmasının yeni sürümüne başvuran yapılandırılmış model eşleme yapılandırmasının önkoşullarını güncelleştirebilirsiniz. 

> [!NOTE]
> Uygulama meta verileri hakkında bilgi elde etmenin bu yolu, yerel işletme verileri (LBD) veya şirket içi olarak dağıtılmış uygulamalar için kullanılabilecek tek yoldur (dağıtım modeli Dynamics 365 for Finance and Operations için kullanılır).
        
