---
title: "Perakende kanalı için mali tümleştirme"
description: "Bu konu, Retail POS için mali entegrasyon genel görünümünü sağlar."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: tr-tr
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a>Perakende kanalı için mali tümleştirme

[!include [banner](../includes/banner.md)]

Bu konu Microsoft Dynamics 365 for Retail'da kullanılabilir olan mali tümleştirme işlevinin genel açıklamasıdır. Mali tümleştirme işlevi, Perakende sektöründe dolandırıcılığı önlemeyi amaçlayan mali yerel yasaları desteklemek için tasarlanmış bir işlevdir. Mali tümleştirme kullanarak kapsanabilen tipik senaryolar:

- Mali makbuz yazdırmak ve bunu müşteriye vermek.
- Satışla ilgili bilgilerin gönderilmesinin ve POS üzerindeki iadelerin yetkili tarafından sağlanan harici bir hizmete gönderilmesinin güvenliğini sağlama.
- Yetkili tarafından yetkilendirilmiş bir dijital imzayla veri koruması kullanma.

Bu konu, kullanıcılar aşağıdaki görevleri gerçekleştirebilsin diye mali entegrasyon kurulumu ayarlamak için yönergeler sağlar. 

- Kaydetme, dijital imzalar ve mali verilerin güvenli gönderimi gibi mali kayıt amaçları için kullanılan mali aygıt ya da hizmetler olan mali konnektörler konfigüre edin.
- Mali belge oluşturma algoritması ve bir çıktı yöntemi tanımlayan belge sağlayıcı konfigüre edin.
- Adımlar sıralaması ve her adımda kullanılan bir grup bağlayıcı tanımlayan mali kayıt işlemi yapılandırın.
- POS işlevsellik profilleri için mali kayıt işlemleri atayın.
- Donanım profilleri (yerel mali bağlayıcılar için) veya (diğer mali bağlayıcı türleri için) POS işlevsellik profillerine bağlayıcı teknik profilleri atayın.

## <a name="fiscal-integration-execution-flow"></a>Mali tümleştirme yürütme akışı
Aşağıdaki senaryo, ortak mali tümleştirme yürütme akışı gösterir.

1. Mali kayıt sürecinin başlatılması.
  
   Perakende hareketinin tamamlanmasından sonrası gibi mali kayıt gerekli olduğu bazı eylemler gerçekleştirdikten sonra, mali kayıt işlemi geçerli POS işlevsellik profili ile ilişkilendirilir.

1. Mali bağlayıcı arayın.
   
   Mli kayıt işlemindeki her mali kayıt adımı için sistem mali bağlayıcı listesi eşleştirir. Bu bağlayıcılar, belirtilen bağlayıcı grubuna dahil olan işlevsel profile sahiptir; mevcut donanım profiliyle (yalnızca **Yerel**e eşit olan bağlayıcı türü için) veya geçerli POS işlevsellik profili (diğer bağlayıcı türleri için) ilişkili bir teknik profil bağlayıcı listesine sahiptir.
   
1. Mali tümleştirme gerçekleştirin.

   Sistem, bulunan bağlayıcıyla ilişkili bir derleme tarafından tanımlanan tüm gerekli olan eylemleri yürütür. Bu işlev profili ve bu bağlayıcı için önceki adımda bulunan teknik profilin ayarlarına göre yapılır.

## <a name="setup-needed-before-using-fiscal-integration"></a>Mali tümleştirme kullanmadan önce kurulum gerekir
Mali tümleştirme işlevini kullanmadan önce aşağıdaki ayarları tanımlarsınız:

- Mali işlev profili numarası için **Perakende parametreleri**nde numara sırasını tanımlayın.
  
- Aşağıdaki referanslar için **Perakende paylaşılan parametreleri** sayfasında numara serileri tanımlayın:
  
  - Mali teknik profil numarası
  - Mali bağlayıcı grubu numarası
  - Kayıt işlemi numarası

- **Mali bağlayıcı**'yı **Perakende > Kanal Kurulumu > Mali tümleştirme > Mali bağlayıcılar**'da oluşturun; mali tümleştirme amaçları için kullanmayı planladığınız her aygıt veya hizmet için.

-  Tüm mali bağlayıcılar için **Mali belge sağlayıcı**'yı **Perakende > Kanal Kurulum > Mali tümleştirme > Mali belge sağlayılar**'da oluşturun. Veri eşleme mali belge sağlayıcının bir parçası olarak kabul edilir. Aynı bağlayıcı için farklı veri eşlemeleri (örneğin, özel durum düzenlemeleri), farklı mali belge sağlayıcıları oluşturmanız gerekir.

- Her mali belge sağlayıcısı için **Bağlayıcı işlev profili**'nde **Perakende > Kanal kurulumu > Mali tümleştirme > Bağlayıcı işlev profilleri** oluşturun.
  - Bir bağlayıcı adı seçin.
  - Bir belge sağlayıcı seçin.
  - **Hizmet Kurulumu** sekmesinde KDV oranları ayarlarını belirtin.
  - KDV kodu eşlemesi ve ödeme türü eşlemesini **Veri eşleme** sekmesinde belirtin.

  #### <a name="examples"></a>Örnekler 

  |  | Biçim | Örnek | 
  |--------|--------|--------|
  | KDV oranı ayarları | değer: VATrate | 1 : 2000, 2 : 1800 |
  | KDV kodları eşlemesi | VATcode : değer | vat20: 1, vat18: 2 |
  | Ödeme türleri eşlemesi | TenderTyp: değer | Nakit: 1, Kart: 2 |

- **Mali bağlayıcı grupları**'nı **Perakende > Kanal kurulumu > Mali tümleştirme > Mali bağlayıcı grubu**nda oluşturun. Bağlayıcı grubu, aynı işlevleri gerçekleştiren ve mali kayıt sürecinde aynı aşamada kullanılan mali bağlayıcılarla ilişkili işlevsel profillerin alt grubudur.

   - Konnektör grubuna işlevsel profiller ekleyin. **İşlevsel profiller** sayfasında **Ekle**'ye tıklayın ve profil numarası seçin.
   - İşlev profili kullanımı askıya almak istiyorsanız, **Devre dışı bırakma** için **Evet**'i seçin. 
   
     Bu değişikliği yalnızca geçerli bağlayıcı grubu etkiler. Bağlayıcı başka gruplarda aynı işlev profili kullanarak devam edebilirsiniz.

     >[!NOTE]
     > Bağlayıcı grup içinde her mali connector yalnızca bir işlev profili olabilir.

- Her mali bağlayıcı için **Bağlayıcı teknik profili**'nde **Perakende > Kanal kurulumu > Mali tümleştirme > Bağlayıcı teknik profilleri** oluşturun.
  - Bir bağlayıcı adı seçin.
  - Bir bağlayıcı türü seçin: 
      - **Yerel** - Bu türü fiziksel aygıt ya da yerel makine üzerinde yüklü uygulamalar için ayarlayın.
      - **Dahili** - Bu türü, mali aygıt ve Retail sunucusuna bağlı servisler için seçin.
      - **Harici** - Vergi dairesi tarafından sağlanan bir web portalı gibi harici mali hizmetler için.
    
  - **Bağlantı** sekmesinde ayarları belirtin.

      
 >[!NOTE]
 > İşlevsel ve teknik profilleri için daha önce yüklenen konfigürasyonun güncelleştirilmiş bir sürümü yüklenir. Uygun bir bağlayıcı veya belge sağlayıcısı zaten kullanılıyorsa, size bildirilir. Varsayılan olarak, işlev ve teknik profillerinde el ile yaptığınız tüm değişiklikler depolanır. Bu profilleri varsayılan parametreler yapılandırma kümesiyle geçersiz kılmak için **Güncelleştir**'e tıklayın: **Bağlayıcı işlev profilleri** sayfası ve **Bağlayıcı teknik profilleri** sayfasında.
 
- **Mali kayıt işlemi**'ni **Perakende > Kanal kurulumu > Mali tümleştirme > Mali kayıt işlemleri**'nde, mali tümleştirmenin benzersiz her işlemi için oluşturun. Bir kayıt işlemi, kayıt adımları ve her adımda kullanılan bağlayıcı grubu dizisi ile tanımlanır. 
  
  - İşlem için kayıt adımları ekleyin:
      - **Ekle** seçeneğini tıklatın.
      - Bir bağlayıcı türü seçin.
      
      >[!NOTE]
      > Bu alan, sistemin bağlayıcının teknik profilinde arama yapacağı yeri belirtir: **Yerel** bağlayıcı türü için donanım profilleri veya diğer mali bağlayıcı türleri için POS işlevsellik profilleri.
      
   - Bağlayıcı grubu seçin.
   
     >[!NOTE]
     > **Doğrula**'ya tıklatıp kayıt işlemi yapısının bütünlüğünü denetleyin. Doğrulamaların aşağıdaki durumlarda yapılması önerilir:
       >- POS işlev profillerini ve donanım profillerini bağlama dahil tüm ayarlar tamamlandıktan sonra yeni kayıt işlemi için.
       >- Güncelleştirmeleri varolan bir kayıt işlemine yapıldıktan sonra.

-  Mali kayıt süreçlerini POS işlevsellik profillerine **Perakende > Kanal Kurulum > POS Kurulum > POS profilleri > İşlevsellik profilleri**'nde bağlayın.
   - **Düzenle**'ye tıklayın ve **İşlem numarası**'nı **Mali kayıt işlemini** sekmesinde seçin.
- Donanım profillerine bağlayıcı teknik profillerini **Perakende > Kanal Kurulum > POS Kurulum > POS profilleri > Donanım profilleri**'nde bağlayın.
   - **Düzenle**'ye tıklayın, ardından **Yeni**'yi **Mali teknik profil** sekmesinde seçin.
   - Bağlayıcı teknik profilini **Profil numarası** alanında seçin.
   
     >[!NOTE]
     > Çok sayıda teknik profilleri, bir donanım profiline ekleyebilirsiniz. Ancak, herhangi bir grup bağlayıcıyla birden çok kesişimi olan donanım profili varsa, bu desteklenmiyor. Yanlış ayarları önlemek için tüm donanım profilleri güncelleştirildikten sonra kayıt işlemini doğrulamanız önerilir.

