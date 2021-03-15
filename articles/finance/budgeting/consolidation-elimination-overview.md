---
title: Birleştirme ve elemeye genel bakış
description: Bu makale konsolidasyon ve eleme işlemleri hakkında genel bilgi sağlar. Sık sorulan bazı soruların yanıtlarını içerir.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee029e6cf1f271c5839e8d0dc1b1e4b7f91fb9a2
ms.sourcegitcommit: f51ef395f0c0cb2203ce26b4091bbf0296e7916e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5120491"
---
# <a name="consolidation-and-elimination-overview"></a>Birleştirme ve elemeye genel bakış

[!include [banner](../includes/banner.md)]

Bu makale konsolidasyon ve eleme işlemleri hakkında genel bilgi sağlar. Sık sorulan bazı soruların yanıtlarını içerir.

Verileri birleştirdiğinizde birden fazla bağlı şirket için finansal sonuçlar tek bir, konsolide şirket sonuçlarında bir araya getirilir. Bağlı kuruluşlar farklı sürümlerde veya sistemlerde bulunuyor olabilir, sahibi farklı olabilir ve farklı para birimleri kullanıyor olabilir. Verilerin birleştirilmesi için birden fazla seçenek mevcuttur:

-   **Çevrimiçi birleştirme** – Bu seçenek, günlük bakiyeleri seçilen hesaplara ve boyutlara göre birleştirir ve bunları bir konsolide şirkette saklar.
-   **Finansal raporlama** – Bu seçenek, hareketlerin ve bakiyelerin birleştirilmesini etkinleştirir ve istenildiği anda oluşturulabilir. Birden fazla hiyerarşi düzeyi oluşturulabilir ve birden fazla raporlama para birimi görüntülenebilir.
-   **İçe aktarmayla birleştirme** – Bu seçenek, bakiyeleri bir konsolide şirkete aktarır.
-   **Şirket bakiyelerini dışa aktarma** – Bu seçenek, şirket bakiyeleri için bir dışa aktarma dosyası sağlar. Dosya daha sonra diğer sürümlere veya sistemlere aktarılabilir. Finansal raporlama da bakiyelerin bir Microsoft Excel dosyasına aktarılması için kullanılabilir.

Elemeler birden fazla yolla raporlanabilir:

-   Eleme kuralları, sistemde oluşturulabilir ve ardından konsolidasyon süreci sırasında veya bir eleme teklifi yoluyla işlenebilir. Kurallar, tüzel kişilik kurulumunda **Mali eleme süreci için kullan** seçimi yapılmış şirketlerin tümüne nakledilebilir.
-   Eleme hareketlerinin el ile belirlenmesi ve nakledilmesi için ayrı bir şirket oluşturulabilir ve kullanılabilir. Bu şirket, konsolidasyon sürecinde veya mali raporlamada kullanılabilir.
-   Şirketler arası faaliyetin belirlenmesi için kullanılan hesaplar ve mali boyutlar, Mali raporlamadaki bir sıra tanımına veya sütun tanımına göre filtrelenebilir ve ayrıntılı şekilde değerlendirilen özellikler kullanılabilir. Bir hesaplanmış sütun veya satır daha sonra konsolide toplamdan hesapların ve mali boyutların kaldırılması için kullanılabilir.

Çok sayıda konsolidasyon senaryosu bulunmaktadır ve her bir yöntem senaryoları farklı şekilde ele alabilir.

## <a name="frequently-asked-questions"></a>Sıkça sorulan sorular
1.  Elemeleri bir veritabanına nakletmeyi tercih ediyorum. Seçeneklerim nelerdir?

Çok sayıda seçeneğiniz bulunuyor. **Çevrimiçi birleştir** seçeneğini kullanabilir ve süreç sırasında veya bir teklif olarak elemeleri dahil edebilirsiniz. Hareketler daha sonra konsolide şirkete nakledilir. Alternatif olarak, el ile elemeler oluşturduğunuz, ayrı bir şirketiniz olabilir ve ardından bu şirketi Mali raporlamada veya birleştirme sürecinde kullanabilirsiniz.

2.  Konsolide sonuçlara birden fazla raporlama para biriminde ihtiyacımız var.

**Mali raporlama** seçeneği, sınırsız raporlama para birimlerine sahiptir. Veriler, ana hesapta ayarlanan döviz kuru türüne ve para birimi hareket yöntemine dayalı olarak, rapor oluşturma sırasında çevrilir. Ancak, **Çevrimiçi birleştir** seçeneği sadece tek bir raporlama para birimine sahip olduğundan, bu seçeneği kullanıyorsanız her bir raporlama para birimi için bir konsolide şirket gereklidir. **Mali raporlama** seçeneği önerilen yöntemdir.

3.  Her bir şirket için hareket düzeyinde ayrıntılar görmek istiyorum.

Hareket düzeyindeki ayrıntılar, raporlama ağaç tanımına dahil edilen sayıda şirket için görüntülenebileceğinden çözüm, **Mali raporlama** seçeneğidir.

4.  Bütçe planlama veya bütçe kontrolü kullanıyoruz ve bunların birleştirilmesi gerekiyor.

Bütçe planlama veya bütçe kontrol verilerinin birleştirilmesi için çözüm, **Mali raporlama** seçeneğidir.

5.  Bağlı kuruluşlarımız dünyanın dört bir tarafında bulunuyor ve birden fazla hesap planına sahibiz. Verilerimizi birleştirmek için önerilen en iyi yöntem hangisidir?

Birden fazla hesap planınız varsa birden fazla seçeneği kullanabilirsiniz. **Çevrimiçi birleştir** seçeneğini kullanabilir ve ardından ana hesapta veya bir konsolide hesap grubunda tanımlanan konsolidasyon hesabını kullanmayı seçebilirsiniz. Ayrıca, **Mali raporlama** seçeneğini kullanabilir, sıra tanımında mali boyutlara birden fazla bağlantı ekleyebilir ve hesapları eşleyebilirsiniz.

6.  Birden fazla konsolidasyon düzeyine ihtiyacımız var. Diğer bir deyişle, öncelikle Avrupa'daki tüm bağlı kuruluşlarımızı İngiliz Sterlini (GBP) için birleştirmemiz gerekiyor. Ardından, bu verileri alacak ve konsolide tutarı Amerikan Dolarına çevireceğiz. Bunu nasıl yapabiliriz?

Birden fazla konsolidasyon düzeyi gerekiyorsa ve her düzeyde farklı para birimleri kullanılıyorsa **Çevrimiçi birleştir** seçeneğini kullanmanız gerekir. Muhasebeleri ve raporlama para birimleri farklı olan, birden fazla konsolide şirket oluşturulmalıdır. Konsolidasyon işlemi birden fazla yürütülmelidir. **Mali raporlama** seçeneği her zaman her bir kaynak şirketin muhasebe para birimini seçilen para birimine çevirir.

7.  Farklı bir sistemde bağlı şirketlerimiz var. Bunları nasıl birleştirebilirsiniz?

Bakiyeleri bir konsolide şirkette birleştirmek için **İçe aktararak birleştir** seçeneğini kullanın.

8.  Bağlı kuruluşlarımızdan bazılarına sadece ortağız. Bunları birleştirmenin en iyi yöntemi nedir?

Kısmen sahip olduğunuz bağlı kuruluşlar için birden fazla seçeneğiniz bulunuyor. **Mali raporlama** seçeneğini kullanarak, bir raporlama ağaç tanımı oluşturabilir ve sahipliği tanımlayabilirsiniz. Ayrıca, kısmen sahibi olduğunuz tutarı temsil etmesi için bir hesaplanmış satır veya sütun da kullanabilirsiniz. Hatta, azınlık hissenizi bir raporda tek başına bir satır olarak da gösterebilirsiniz. Ayrıca, **Çevrimiçi birleştir** seçeneğini de kullanabilirsiniz. **Tüzel kişilikler** sekmesinde bir **Sahiplik** sütunu bulunur ve buradan ana şirketin sahip olduğu yüzdeyi tanımlayabilirsiniz.

9.  Organizasyonumuzun, ticari birime göre konsolidasyonu göstermesi gerekiyor veya organizasyonumuz organizasyon hiyerarşilerini kullanmak istiyor.

Çözüm, **Mali raporlama** seçeneğidir. Tüzel kişiliklere veya mali boyutlara sahip organizasyon hiyerarşileri, Mali raporlama üzerinden rapor edilebilir. Tüzel kişilikler ile boyut değerlerinin bir birleşimini sahip olan bir raporlama ağaç tanımı kullanarak da kendi çok düzeyli hiyerarşilerinizi oluşturabilirsiniz.

10. Sistemin birden fazla sürümüne sahipsiniz.

Bir sürümden dışa aktarma yapmak için **Şirket bakiyelerini dışa aktar** seçeneğini kullanabilir ve ardından diğer sürümde **İçe aktararak birleştir** seçeneğini kullanarak verileri birleştirebilirsiniz.

11. **TASLAK** durumunda bütçeyle bir konsolidasyon yapabilir miyim? 
            
Konsolidasyon şirketinde bütçeleri işleyemez veya tamamlayamazsınız. Taslak bütçeleri konsolide etmek için Financial Reporting'i kullanmanızı öneririz.

Daha fazla bilgi için bkz. [Konsolidasyon şirketinde para birimi yeniden değerleme](../general-ledger/currency-revaluation-consolidation-company.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]