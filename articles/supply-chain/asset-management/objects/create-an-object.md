---
title: Varlık oluşturma
description: Bu konuda Varlık Yönetimi'nde varlık oluşturma işlemi açıklanmaktadır.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTableCopyStructure, EntAssetObjectTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e9c2b81e97a7b08dfdb596fbf6822ac94c7358dccd0b92c0677467dbc0c2e26
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721523"
---
# <a name="create-an-asset"></a>Varlık oluşturma

[!include [banner](../../includes/banner.md)]

 

Bu konuda Varlık Yönetimi'nde varlık oluşturma işlemi açıklanmaktadır.

1. **Varlık yönetimi** > **Genel** > **varlıklar** > **Tüm varlıklar** veya **Etkin varlıklar**'a tıklayın.
2. **Yeni** düğmesine tıklayın.
3. **Varlık oluştur** iletişim kutusunda, **Varlık** ile ilgili bilgileri (varlık kodu) ve varlık adını girin. **Etkin** alanında varlık için tarih ve saat seçin. Bu tarihten itibaren, varlığı işlem yapılacak bir yerleşime yükleyebilir ve varlığı bir varlık yapısında taşıyabilir ve değiştirebilirsiniz.
4. **Varlık türü** alanında, varlık için varlık türünü seçin (zorunlu alan). Gerekirse, varlık için **Varlık üreticisi** ve **Varlık modeli**'ni seçin. Yalnızca bir ürün ayarlanmışsa, bu ürün **Varlık üreticisi** alanında otomatik olarak seçilir. **Varlık üreticisi** ve **Varlık modeli** alanlarındaki kullanılabilir seçimler, [Varlık üreticileri ve modelleri](../setup-for-objects/product-and-model.md)'ndeki ayara bağlıdır.
5. **Üst varlık** grubunda, **Varlık** alanı varsayılan olarak boştur. Gerekirse, bir üst varlık seçebilirsiniz. Bu durumda **Üst varlık** grubundaki tüm alanlar otomatik olarak doldurulur
    >[!NOTE]  
    >Bir üst varlık seçtiğinizde, kullanılabilir iki veya üç sekme bulunur: **Varlıklarım** sekmesi, tahsis edilebileceğiniz (sistemde oturum açan bakım çalışanı) işlem yapılacak yerleşimlerle ilgili varlıkları içerir. [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md) formundaki bir bakım görevlisi için ayarlanmış bir işlem yapılacak yerleşim yoksa **Varlıklarım** sekmesi görünmez. **Etkin varlıklar** sekmesi, varlık yaşam döngüsü durumu "Etkin" olan tüm varlıkların listesini içerir. **Varlık görünümü** sekmesi, işlem yapılacak yerleşimlerin ve bu yerleşimlerde kurulu olan varlıkların ağaç görünümünü gösterir.

6. Ayarladığınız varsayılan işlem yapılacak yerleşim **Varlık** grubu > **İşlem yapılacak yerleşim** alanındaki varlık için önerilir. Gerekirse başka bir işlem yapılacak yerleşim seçin.

    >[!NOTE]
    >Bir varlık oluşturduktan sonra, gerekirse varlığı başka bir işlem yapılacak yerleşime yükleyebilirsiniz. Yalnızca üst düzey varlıklar (geçerli üst varlığı bulunmayan varlıklar) işlem yapılacak yerleşime yüklenebilir. Bu, seçili işlem yapılacak yerleşime üst düzey ve alt düzey varlıkları yüklediğiniz anlamına gelir. Varlıkları, işlem yapılacak yerleşimlere yükleme hakkında daha fazla bilgi için [İşlem yapılacak yerleşimlere giriş](../functional-locations/introduction-to-functional-locations.md) bölümüne bakın.

7. **Tamam**'a tıklayın.
8. **Tüm Varlıklar** listesinde varlığı seçin ve varlığa daha fazla bilgi eklemek için **Düzenle** düğmesine tıklayın.

## <a name="general-information"></a>Genel bilgiler

Varlığın ilişkili olduğu işlem yapılacak yerleşim **İşlem yapılacak yerleşim** alanında gösterilir. Varlık bir üst varlıksa, varlıkla ilgili alt varlıkların sayısı **Alt** alanında gösterilir. Varlık mevcut bir varlığın alt varlığıysa, üst varlığın kodu **Üst** alanında gösterilir.

Varlıktaki yedek parçaları, alternatif yedek parçaları ve iş türü varsayılanlarını yönetmek için kullanılan **Varlık üreticisi** ve **Varlık modeli** bilgilerini düzenleyebilirsiniz. Daha fazla bilgi için bkz. [Varlık üreticileri ve modelleri](../setup-for-objects/product-and-model.md). Gerekirse **Model yılı** ve **Seri numarasıyla** ilgili bilgi de ekleyebilirsiniz.

**Geçerli yaşam döngüsü durumu** varlığın etkin mi yoksa devre dışı mı olduğunu tanımlamak için kullanılır. Bir varlık oluştururken, aşama her zaman varlık aşama grubundaki ilk aşamaya ayarlanır. Bir varlığı etkinleştirmeye hazır olduğunuzda **Varlık durumunu güncelleştir**'e tıklayın ve "varlık etkin" olarak tanımladığınız yaşam döngüsü durumunu seçip **Tamam**'a tıklayın.

**Not:** Bir varlık "etkin değil" olarak ayarlandığında, bu varlık için iş emirleri oluşturmak mümkün değildir. Ayrıca, etkin olmayan bir varlık için önleyici bakım işleri zamanlayamazsınız.

**Hizmet düzeyi** ve **Kritiklik** alanları varlık için oluşturulan iş emirleriyle ilgilidir. Alanlar, varlığa ilişkin geçerli kurulum için hesaplanan **Hizmet düzeyi** ve **Kritiklik** sayılarını gösterir. Bu değerlerin ayarlanmasıyla ilgili olarak [Varlık hizmet düzeyleri](../setup-for-objects/object-priorities.md) ve [Varlık kritiklik türleri](../setup-for-objects/object-criticalities.md)'ne bakın.

## <a name="asset"></a>Aktif

Varlık için bir **Kaynak** seçebilirsiniz. Kaynak seçimi, iş emri planlaması için hangi takvimin kullanılacağını belirler. Kaynak seçimi genellikle sabit kıymetler için kullanılır. Kaynaklar ve kaynak grupları **Kuruluş Yönetimi** > **Kaynaklar** > **Kaynak grupları** veya **Kaynaklar**'da ayarlanır.

**Sabit kıymet sayısı** alanında, varlıkla ilişkilendirilecek bir sabit kıymet seçebilirsiniz. Bu varlığınızın bir yatırım projesiyle ilgili olması durumunda geçerlidir.

- Varlık bir sabit kıymetle ilgiliyse, bir yatırım projesiyle ilgili iş emirleri için kullanılacak bir iş emri türü oluşturabilirsiniz. 
- Bir varlığın sabit kıymetleri hakkındaki bilgiler, Dynamics 365 Supply Chain Management'daki **Sabit kıymetler** modülüyle ilişkilidir. Bu, **Sabit kıymetler** > **Sabit kıymetler** > **Sabit kıymetler**'de, listedeki bir varlığı seçip **İlgili bilgiler** bölmesi > **İlişkili projeler** bölümündeki içerikleri görüntüleyerek bir sabit kıymetle ilgili olabilecek Varlık Yönetimi projelerine genel bakış yapabileceğiniz anlamına gelir.


## <a name="details"></a>Ayrıntılı

**Etkin olma başlangıcı** alanında, varlık yaşam döngüsü durumunu etkin duruma güncelleştirdiğiniz tarih (Varlık yaşam döngüsü durumları ayarrıyla ilgili [Varlık yaşam döngüsü durumları](../setup-for-objects/object-stages.md) konusuna bakın) gösterilir. Varlık artık etkin değilse ve varlık yaşam döngüsü durumunu etkin olmayan bir yaşam döngüsü durumuna güncelleştirdiyseniz, varlığın etkin olmamaya başladığı tarih **Etkin olma bitişi** alanında gösterilir. Gerekirse, butarihleri el ile değiştirebilirsiniz.

Gerekirse, **Değiştirme tarihi** alanına varlığın değiştirilmesi için beklenen bir tarih ekleyebilirsiniz. Varlığı değiştirmek için tahmini bir değer **Değiştirme değeri** alanına eklenebilir. Örnek: Değiştirme bilgilerini, bir varlığın korunması maliyetleriyle karşılaştırmak için kullanabilirsiniz ve daha sonra mevcut varlığın bakım maliyetleri hızla artırsa yeni bir varlık satın alma kararı alabilirsiniz.

## <a name="notes"></a>Notlar

**Notlar** hızlı sekmesinden varlıkla ilgili notlar ekleyebilirsiniz. Nota kullanıcı bilgilerini ve tarih/zaman damgası eklemek isterseniz notu yazmadan önce **Zaman damgası ekle** düğmesine tıklayın.

## <a name="attributes"></a>Öznitelikler

Bu hızlı sekmede, varlık öznitelikleri için değerler ayarlayabilirsiniz. Bu öznitelikler, varlıkla ilgili boyut, ağırlık veya makine yapılandırması gibi özellikleri veya teknik özelliklerini açıklamak için kullanılabilir.

**Satır ekle**'ye tıklayın ve öznitelik türünü seçin. Ardından, öznitelik türü ile ilgili **Değeri** ekleyin ve kaydı kaydedin.

>[!NOTE] 
>**Varlık özniteliği** ve **Varlık özniteliğine genel bakış**'tan varlık öznitelik türleri ve varlıklarla ilişkileri hakkında genel bir bakış edinebilirsiniz. Daha fazla bilgi için bkz. [Varlık özniteliğine genel bakış](../objects/object-specification-overview.md).

## <a name="vendor"></a>Satıcı

**Satıcı** hızlı sekmesinde, varlık için bir satıcı hesabı seçin. Ayrıca, bir satıcı garantisi verilmişse, garanti bilgilerini buraya ekleyebilirsiniz.

## <a name="address"></a>Adres

**Adres** hızlı sekmesinde, ekipmanın adresini ekleyebilirsiniz. Varlığa hiçbir adres eklenmezse, varlık üst varlığın adresi varsa üst varlığın adresini kullanır. Varlık hiyerarşisindeki varlık veya üst varlıklarla ilgili adres yoksa, varlığın yüklü olduğu işlem yapılacak yerleşimin adresi kullanılabilir. Bu işlem yapılacak yerleşime ait ilgili bir adres yoksa, varlıktaki üst işlem yapılacak yerleşimin adresi kullanılır.

## <a name="asset-management-plans"></a>Varlık yönetimi planları

Bakım planları, varlık üzerinde düzenli aralıklarla önleyici bakım işleri planlamak için kullanılır. Bu hızlı sekmede, seçili varlık için bakım planı satırları ayarlayabilirsiniz. Bakım sıraları, düzenli aralıklarla benzer bir görevi gerçekleştirmeniz gereken çeşitli varlıklar için ayarlanabilir. **İşlem yapılacak yerleşim bakım planları** sekmesinde, varlığın yüklü olduğu işlem yapılacak yerleşimlerle ilgili bakım planlarını görürsünüz.

>[!NOTE]
>**Tüm Varlıklar**'da bir varlıkla ilgili bakım planı satırını veya bakım sırasını silerseniz, bu bakım planını veya bakım sırasını temel alarak oluşturulan "Oluşturuldu" durumundaki tüm bakım zamanlamalarını da otomatik olarak silersiniz.

## <a name="functional-location-maintenance-plans"></a>İşlem yapılacak yerleşim bakım planları

Bu hızlı sekmede, varlığın yüklü olduğu işlem yapılacak yerleşimlerle ilgili bakım planlarına genel bakışı görürsünüz.

## <a name="maintenance-rounds"></a>Bakım sıraları

Bu hızlı sekmede, varlıkla ilişkili bakım sıraları ekleyebilir veya kaldırabilirsiniz.

## <a name="financial-dimensions"></a>Mali boyutlar

Varlık için mali boyutları seçebilirsiniz.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]