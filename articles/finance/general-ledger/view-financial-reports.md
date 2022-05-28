---
title: Mali raporları görüntüleme
description: Bu konuda, Microsoft Dynamics 365 Finance'te mali raporların nasıl görüntüleneceği ve keşfedileceği açıklanmaktadır. Görünümlerini ve içerdikleri veriyi değiştirmek için finansal raporlara uygulayabileceğiniz çeşitli seçenekler hakkında bilgiler içerir.
author: kweekley
ms.date: 03/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fec130ce7b05a8e0b8182a63679cf7b20983f1d0
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724429"
---
# <a name="view-financial-reports"></a>Mali raporları görüntüleme

[!include [banner](../includes/banner.md)]

Bu konuda, mali raporların nasıl görüntüleneceği ve keşfedileceği açıklanmaktadır. Görünümlerini ve içerdikleri veriyi değiştirmek için finansal raporlara uygulayabileceğiniz çeşitli seçenekler hakkında bilgiler içerir.

## <a name="financial-reporting-overview"></a>Mali raporlamaya genel bakış

## <a name="open-a-financial-report"></a>Bir mali rapor açma
Bir rapor açmak için raporun adını seçin. Bir rapor ilk defa açıldığında otomatik olarak önceki ay için oluşturulur. Örneğin, bir raporu ilk kez Ağustos 2015'te açarsanız rapor 31 Temmuz 2015 tarihi için oluşturulur. Rapor açıldıktan sonra, belirli veri parçalarında ayrıntıya inerek ve rapor seçeneklerini değiştirerek keşfetmeye başlayabilirsiniz.

## <a name="drill-down-on-a-financial-report"></a>Bir mali raporu ayrıntılı inceleme
Mali raporlar birden çok ayrıntı düzeyi içerebilir. Mali düzey bir mali raporu ilk defa açtığınızda gördüğünüz düzeydir. Muhasebe düzeyine gitmek için ayrıntılı şekilde gözden geçirilecek verileri seçin. Örneğin, satışlar için hesap ayrıntılarını görmek için derinlemesine incelemek istediğiniz satış verilerini seçin. Hesap düzeyinden, hesap bakiyesini oluşturan hareketleri görüntüleyebilirsiniz. Hareketlerin görüntülenmesi için rapor hareketleri ve fiş hareketleri olmak üzere iki yöntem mevcuttur.

-   **Rapor hareketleri** – Biçimlendirilmiş bir görüntüde gözüken hareketler, mali rapora dahil edilir. Hareketleri biçimlendirilmiş görünümde görüntülemek için derinlemesine incelenecek verileri seçin ve ardından **Rapor hareket düzeyine git** düğmesini tıklayın.
-   **Fiş hareketleri** – Bir fiş hareketi sorgusu açılır ve hareketleri görmenizi sağlar. Fiş hareketi sorgusundaki hareketleri görüntülemek için derinlemesine incelenecek verileri seçin ve ardından **Hesap hareketlerini aç** düğmesine tıklayın.

Veriler bütçe verileri ise, bütçe hesabı girişlerini açmayı seçebilirsiniz. Raporun herhangi bir düzeyini kapatmak ve başladığınız yere dönmek için, Esc tuşuna basabilir veya sağ üst köşedeki **Kapat** düğmesini (**X**) tıklayabilirsiniz.

## <a name="change-report-options"></a>Rapor seçeneklerini değiştirme
Bir **Fiili - bütçe**, öznitelik ve boyut filtreleri uygulayabilir veya bütçe senaryosunu değiştirebilirsiniz. Eylem Panosunda **Rapor seçenekleri** düğmesini tıklayın ve ardından bu adımlardan birini veya daha fazlasını takip edin:

-   Bir rapora özellik filtreleri uygulamak için **Bir öznitelik filtresi ekle** öğesini seçin. Özniteliği seçin, öznitelik değerini girin ve ardından **Tamam** düğmesini tıklayın. Örneğin, **Hesap Kategorisi** özniteliğini seçerseniz, öznitelik değeri olarak **SATIŞ** girin. Bir öznitelik filtresini kaldırmak için **Temizle** düğmesini tıklayın.
-   Bir rapora boyut filtreleri uygulamak için **Boyut filtresi ekle** öğesini seçin. Boyutu seçin ve boyut kodunu yazın veya listeden boyutu seçin. Bir boyut filtresini kaldırmak için **Temizle** düğmesini tıklayın.
-   Bir **Fiili - bütçe** raporundaki senaryoyu değiştirmek için yeni bir senaryo seçin ve ardından **Tamam** düğmesini tıklayın. Seçilen senaryo farklı bir mali yıldaysa, herhangi bir sonuç döndürülmez. Örneğin, bir rapor FY2015 için oluşturulursa ve geçerli senaryo FY2015 içinse ve yeni senaryo FY2016 için seçilirse, hiçbir sonuç döndürülmez. Farklı bir mali yıl için yeni bir senaryo gerekliyse, senaryoyla ilişkili mali yıl için raporun yeni bir sürümünü oluşturun.

**Tamam** düğmesini tıkladığınızda, seçtiğiniz tüm seçenekler rapora uygulanır. Seçilen seçenekleri uygulamak istemediğinize karar verirseniz **İptal** düğmesini tıklayın.

## <a name="update-a-financial-report"></a>Bir mali raporu güncelleştirme
Bir mali raporu, raporun oluşturulduğu dönem ve yıl için en son verileri gösterecek şekilde yenileyebilir (güncelleştirebilirsiniz). Örneğin, Ekim 2015 için oluşturulan bir mali raporu güncelleştirdiğinizde rapor, Ekim 2015'ten sonra nakledilen tüm yeni hareketleri de gösterecektir. Bir mali raporu güncelleştirmek için Eylem Panosundan **Yenile** düğmesini tıklayın. Güncelleştirilen rapor sadece raporu güncelleştiren kişiye açık olacaktır. Başka insanların da aynı verileri görebilmesi için rapor mutlaka yayınlanmalıdır.

## <a name="publish-a-financial-report"></a>Bir mali rapor yayınlama
Bir mali rapor güncelleştirdikten sonra yayımlayabilirsiniz. Bu durumda organizasyonunuzdaki diğer kişiler de raporu görebilir. Bir raporu yayınlamak için Eylem Panosundan **Yayınla** düğmesini tıklayın.

## <a name="display-a-financial-report-in-a-different-currency"></a>Bir mali raporu başka bir para biriminde gösterme
Bir mali rapor istenildiği anda istenilen bir para biriminde görüntülenebilir. Bir raporu farklı bir para biriminde göstermek için Eylem Panosundan **Para Birimi** düğmesini tıklayın ve ardından bir para birimi seçin. Rapor, seçilen para birimine çevrilerek sonuçlar görüntülenir. Rapor tasarımının bir parçası olarak dahil edilen tüm para birimi kodları veya simgeleri yeni para birimini yansıtacak şekilde güncelleştirilir. Listede görüntülenen para birimleri, Finance'te yapılandırılan raporlama para birimleridir.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Mali raporun bir özet görünümünü görüntüleme
Bir mali rapor ayrıntılı satırlar ve özet satırlar içerebilir. Ayrıntılı satırlar çok sayıda hesap veya boyut içeren satırlardır. Özet satırları açıklama, toplam ve hesaplama satırlarıdır. Bir raporun yalnızca özet satırlarını görüntülemek için tıklatın **Göster** düğmesini ve ardından **Sadece özet satırları** düğmesini tıklayın. Rapor daraltılır ve sadece özet satırlarını görüntüler. Ayrıntılı satırları özet satırlarıyla birlikte görüntülemek için **Göster** düğmesini tıklayın ve ardından tekrar **Sadece özet satırları** düğmesini tıklayın.

## <a name="print-a-financial-report"></a>Bir mali rapor yazdırma
Bir mali raporu yazdırmak, daha sonra el ile yazdırılabilecek bir PDF dosyası oluşturur. Yazdırılabilir bir mali rapor oluşturmak için Eylem Panosundan **Yazdır** düğmesini tıklayın ve yazdırma seçeneklerini ayarlamak için bu adımlardan birini veya birden fazlasını takip edin:

-   Farklı ayrıntı düzeylerini yazdırılan rapora dahil etmek için kaydırıcıyı **Evet** veya **Hayır** konumuna ayarlayın. Bir rapor bir raporlama ağacı kullanıyorsa tüm raporlama birimlerini veya sadece mevcut raporlama birimini dahil etmeyi seçebilirsiniz.
-   Sayfa boyutunu ayarlamak için listeden bir sayfa boyutu seçin.
-   Sayfa düzenini ayarlamak için listeden bir düzen seçin. Rapor içeriği seçtiğiniz genişliğe sığdırmak istiyorsanız kaydırıcıyı **Evet** konumuna ayarlayın.
-   Sayfa kenar boşluklarını ayarlamak için üst, alt, sol ve sağ kenar boşluklarının boyutunu inç cinsinden girin.

Yazdırma seçeneklerini ayarlamayı bitirdikten sonra, devam etmek için **Yazdır**'ı tıklayın ve dosyayı indirmek mi istediğiniz yoksa OneDrive veya SharePoint üzerine kaydetmek mi istediğiniz sorulur. Devam istemediğinize karar verirseniz bunun yerine **İptal** düğmesini tıklayın. Devam ettiğinizde, rapor sunucuda işlenmeye başlar ve raporu PDF biçiminde indirmeniz size sunulur. Şimdi raporu PDF görüntüleyicinizde görüntüleyebilir ve buradan raporun gönderileceği yazıcıyı seçebilirsiniz ve yazdırma seçenekleri için daha fazla ayar yapabilirsiniz.

## <a name="export-a-financial-report"></a>Bir mali raporu dışa aktarma
Bir mali raporu dışa aktarmak için Eylem Panosundan **Dışa aktar** düğmesini tıklayın. Rapor, Microsoft Excel'e aktarılır ve tarayıcınız dışa aktarılan dosyayı açmak mı, yoksa kaydetmek mi istediğinizi sorar. Rapor tasarımında ayarlanan dışa aktarma ayarları dışa aktarılan rapora uygulanır.    

## <a name="additional-resources"></a>Ek kaynaklar

[Mali raporlama](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
