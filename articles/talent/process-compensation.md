---
title: "Ücret işleme"
description: "Ücret işleme, öz varlık düzenlemeleri, başarı artışı hedefleri ve performansı temel alarak personelinizin yeni taban ücret tutarlarını hesaplamanıza olanak tanır."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 0886f60dbdfc531893cd2c1b23df5b52a4a2f4b6
ms.contentlocale: tr-tr
ms.lasthandoff: 03/08/2018

---

# <a name="process-compensation"></a>Ücret işleme

[!include [banner](includes/banner.md)]

Ücret işleme, öz varlık düzenlemeleri, başarı artışı hedefleri ve performansı temel alarak personelinizin yeni taban ücret tutarlarını hesaplamanıza olanak tanır. Bu konu, bir personelin performansını değerlendirmeye katılmadan sabit ücret planları için ücret işleme temel akışını ele almaktadır.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Yeni ücret tutarlarını ve bütçeleri planlama
Personelinize başarı artışı vermek için, tüm Departmanlarınız için sabit artış bütçesi ayarlamanız gerekir: Ücret yönetimi > Bağlantılar > Başarı artışı hedefleri. (Alternatif olarak, bu formu Departman > Kuruluş > Departmanlar öğeleri aracılığıyla da açabilirsiniz.) Burada, bazı iş birimindeki veya konumdaki personelin farklı bir artış yüzdesi alıp almayacağını belirtebilirsiniz. **Bütçe** ve **Para birimi** alanları bilgi amaçlıdır ve bütçe için bir para birimi tutarı not etmek için kullanılabilir.

## <a name="set-up-the-compensation-process"></a>Ücret işlemini ayarlama
Bir işlem olayı ücret işleme parametreleri belirtmenize olanak verir. Bu ücretlendirme tutarlarını belirlemek için değerleme tarih aralığını ve yeni ücret tutarlarının etkin olacağı tarihi içerir.

Sabit ücret planlarınız Yüzde türünde işe alma kuralı kullanıyorsa, isteğe bağlı olarak sabit ödemeli eşit dağıtılmış işe alma tarihi de ekleyebilirsiniz. Bu planlar için döngü başlangıç tarihinden sonra ve sabit ödemeli eşit dağıtılmış işe alma tarihinden önce işe alınan bir kişi hesaplanan başarı veya genel artışının %100'nü alacaktır. Sabit ödemeli eşit dağıtılmış işe alma tarihinden sonra ve döngü bitiş tarihinden önce işe alınan bir kişi, işe alındığında toplam döngü gün sayısından kaç gün geçtiği temel alınarak hesaplanan artışın bir bölümünü alır. Örneğin döngü 1 Ocak ile 31 Aralık arasındaysa ve 1 Nisan tarihli sabit ödemeli eşit dağıtılmış işe alma tarihimiz varsa, Mart ayında işe alınan personel hesaplanan tam artışı alırken 1 Temmuz tarihinde işe alınan bir personel yaklaşık olarak hesaplanan artışın yarısını alır.

İşlem olayı **Belirli bir nokta** tarihi, yalnızca belirli değişken ücret planlarını işlemek için kullanılır ve burada açıklanmaz. **İnceleme son tarihi** tüm önerileri yapmak için son tarihtir, böylece yeni ücret tutarları personelin kaydına yüklenebilir. İnceleme tarihi yalnızca bilgilendirme amaçlıdır.

İşlem olayı parametreleri kaydedildikten sonra, bu işlemin çalıştırılmasına dahil edilecek planları ve her plan için hangi sabit ücret eylemlerinin gerçekleştirileceğini dahil etmek üzere **Kurulum** düğmesini tıklayabilirsiniz.

**Planlar** sekmesindeki **Ekle** düğmesini tıklayarak işlem olayına bir ücret planı ekleyin. **Başka dengeleme kullan**, **Dengeleme faktörü** ve **Dengeleme açıklaması** sütunları yalnızca değişken ücret planları için kullanılır ve bu konuda ele alınmamaktadır.

Kaydı kaydedin ve **Eylemler** sekmesindeki **Ekle** düğmesini tıklayarak seçili plan için sabit ücret eylemleri ekleyin. Eylem için hesaplanan rehber artıştan farklı bir tutar girmek için **Öneriyi etkinleştir** seçeneğini kullanın. Birden fazla ücret eylemini bağlamak için bir eylemin önceki eylemin sonucu temel alınarak hesaplanması amacıyla, **Önceki sonucu kullan** seçeneğini seçin Sabit ücret eylemleri aynı zamanda açıklayıcı isimler verebileceğiniz ücret mantığı türleridir. Derece ve Bant planları için yalnızca aşağıdaki türde sabit ücret eylemleri ekleyebilirsiniz:

| Sabit ücret eylemi türü | İşlev                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Öz Varlık                        | Öz varlık eylemleri personelin döngü bitiş tarihi itibarıyla ödeme oranını personelin işinde belirtilen düzey için en alt referans noktasıyla karşılaştırır. Personelin ödeme oranı minimum referans noktasından daha küçükse, aralık içinde personel için minimum noktaya getirmek için gerekli artış hesaplanır.                                                                                |
| Liyakat                         | Başarı eylemleri artışı personelin döngü bitiş tarihi itibarıyla ödeme oranını ve personelin departmanı, iş birimi veya konumu için sabit artış bütçesinde yer alan artış yüzdesini temel alarak hesaplar.                                                                                                                                                                                         |
| Genel                       | Genel eylemler artışı Yüzdeyi temel alarak hesaplar veya personele bir sabit tutar verir. Bu, **Genel** sekmesinin **Sabit ücret** ayarlarına göre belirlenir.                                                                                                                                                                                                                        |
| Terfi                     | Promosyon eylemleri artışlarla ödüllendirme yapabileceğiniz adlandırılmış bir yer sağlar, bu nedenle promosyon alacak personel için öneri girebilmek için **Öneriyi etkinleştir** seçeneğini işaretlediğinizden emin olun.  Önerilen artışı bulunmayan personelin sabit ücret kaydına **Promosyon** eylemi eklenmez.                                                                       |
| Diğer düzey değişikliği            | Önceki örnekte, **Derece indirme** **Diğer düzey değişikliği** türüne sahip **Sabit ücret** eylemimizin adıydı. Bu 0 (sıfır değişiklik) kılavuz artış oluşturur böylece personelin ödeme oranını düzenlemek için bir öneri tutarı girebilirsiniz. (**Öneriyi etkinleştir** seçeneğini etkinleştirdiğinizden emin olun.) Öneri bulunmayan personelin sabit ücret kaydına bu eylem eklenmeyecektir. |

Yalnızca Adım Adım plan türüne sahip **Sabit ücret** eylemleri ekleyebilirsiniz.

| Sabit ücret eylemi türü | İşlev                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aşama                           | Genel sekmesinde, bu Adım eyleminin çalışanları 0 adım mı, 1 adım mı yoksa 2 adım mı ilerletmesi gerektiğini belirtin.                                                                                  |
|                                | **0 adım** - Çalışan üzerinde olduğu geçerli adıma göre ödeme oranı alacaktır.                                                                                                                      |
|                                | **1 adım** - Sistem çalışanın kendi düzeyi için zaten en son referans noktasında olup olmadığını kontrol eder.                                                                                             |
|                                | **2 adım** - Sistem çalışanı geçerli düzeyde iki adım ilerletir. Sistem çalışanı yalnızca kendi düzeyindeki son referans noktasına erişmiş olması durumunda bir veya sıfır adım hareket ettirir. |

## <a name="run-the-compensation-process"></a>Ücret işlemini çalıştırma
İşlem olayı gerekli tarih alanları, planlar ve eylemler ile ayarlandıktan sonra **İşlem olayı** sayfasında **İşlemi çalıştır**'a tıklayabilirsiniz. Böylece **Ücret işlem olaylarını çalıştır** iletişim kutusu açılır. Bu iletişim kutusunda **İşlem sonuçlarını göster** seçeneğini tıklayarak ücret tutarlarının her çalışan için nasıl hesaplandığını görebilirsiniz. **Tamam**'ı tıklamak döngü bitiş tarihi itibarıyla seçili ücret planlarında olan tüm çalışanlar için ücret işlemini çalıştırır.

## <a name="view-the-process-results"></a>İşlem sonuçlarını görüntüleme
İşlemin sonuçlarını görmek için **İşlem sonuçları** sayfasını açın. İşlem olayı her çalıştırıldığında yeni bir ücret olayı oluşturulur. Bu şekilde, deneme çalıştırmaları yapabilir, düzenlemeler yapabilir ve ücret olayının birden fazla çalıştırarak çeşitli değişikliklerin çalışan ücretini nasıl etkilediğini görebilirsiniz.

**İşlem sonuçları** sayfası çalıştırmanın ne zaman yapıldığı, işlemi çalıştıran kişi ve işlem çalıştırılırken hata oluşup oluşmadığı da dahil olmak üzere işlem çalıştırmayla ilgili bilgileri içerir. Ayrıca **Ücret yükle** düğmesini devre dışı bırakmak için **Kilitli** seçeneğini işaretleyebilir ve herhangi birinin çalışan kayıtlarına ücret olaylarını yüklemesini önleyebilirsiniz. **Çalışan sonuçları** düğmesini tıkladığınızda çalıştırmaya dahil edilen çalışanların listesi görüntülenir.

**Personel sonuçları** seçeneği,işlemin kendisi ve işlem sırasında gerçekleştirilen ücret eylemler hakkında bilgi gösterir. **Sabit ücret** bölümü, ücret planını işlem olayındaki her bir eylem için bir kayıt içerir. **Geçerli Kılavuz** ve **Öneri** sütunları **Sabit ücret** bölümünde seçilen eylem hakkında daha fazla bilgi görüntüler. **Önerileri etkinleştir** eylem için işaretlenmişse, Öneri alanları düzenlenebilir olacaktır. Bu çalışan için tutarları el ile ayarlamanıza olanak tanır. İşlem olayında eylem için **Önceki sonucu göster** seçeneğini işaretlediyseniz, bağlı her eylem için tutarları el ile güncelleştirmeniz gerektiğini unutmayın.

Ücret tutarlarını bir çalışan için gözden geçirildikten ve önerilen değerler için düzenlemeler yapıldıktan sonra, **Çalışan olayı** satırındaki **Durum**'u olayın onaylanmış olup olmadığını veya yok sayılması mı gerektiğini belirtmek üzere değiştirebilirsiniz. İsteğe bağlı olarak, **Yeniden hesapla** düğmesine tıklayarak çalışan önerisinde yapılan değişiklikleri silebilirsiniz. BU, mevcut çalışan olayını Yoksay durumuyla işaretler ve yeniden hesaplanan değerlerle yeni bir çalışan olayı oluşturur.

## <a name="loading-approved-compensation-changes"></a>Onaylanan ücret değişikliklerini yükleme
Bir veya daha fazla çalışan olayının durumu onaylandı olarak güncelleştirildikten sonra, bu olaylar çalışanların sabit ücret kayıtlarına yüklenebilir. Bu işlem her personel olayını ayrı ayrı seçip **Çalışan sonuçları** sayfasındaki **Personel ücretini yükle** düğmesine tıklayarak veya onaylanan tüm çalışan olaylarını bir kerede yüklemek için **İşlem sonuçları** sayfasındaki **Ücreti yükle**'ye tıklayarak yapılabilir.

**Ücreti yükle** iletişim kutusundaki **Tamam**'a tıklamak **Çalışan sabit ücreti** sayfasına sıfır olmayan ücret eylemi satırları ekleyecektir.

