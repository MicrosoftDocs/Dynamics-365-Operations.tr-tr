---
title: El ile oluşturulmuş iş emirleri
description: Bu konuda Varlık Yönetimi'nde el ile iş emirleri oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a4b148d9ac5d032d2caa5fcea0398a5a3726f0e
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888989"
---
# <a name="manually-created-work-orders"></a>El ile oluşturulmuş iş emirleri

[!include [banner](../../includes/banner.md)]


İş emirlerini el ile iki şekilde oluşturabilirsiniz.

- **Tüm iş emirleri** veya **Etkin iş emirleri** sayfasında 
- **Tüm bakım istekleri** veya **Etkin bakım istekleri** veya **İşlem yapılacak yerleşim bakım isteklerim** sayfasında 

## <a name="create-work-order"></a>İş emri oluştur

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ni seçin.

2. **Yeni**'yi seçin.

3. **İş emri oluştur** iletişim kutusunda **İş emri türü** alanında bir iş emri türü seçin.

4. Gerekirse, bir **Açıklama** seçin.

5. **Varlık** alanında varlığı seçin.

>[!NOTE]
>Bir varlık seçtiğinizde, **Varlık** açılan menüsünde üç sekme bulunabilir: 

- **Etkin varlıklar** - Bu sekme, varlık yaşam döngüsü durumu "Etkin" olan tüm varlıkların listesini içerir. 
- **Varlık görünümü** - Bu sekme, işlem yapılacak yerleşimlerin ve bu yerleşimlerde kurulu olan varlıkların ağaç görünümünü gösterir.
- **Varlıklarım** - Bu sekme, sizin (sistemde oturum açan çalışan) tahsis edilmiş olabileceğiniz işlevsel yerleşimlerle ilgili varlıkları içerir. (Kurulum hakkında bilgi için bkz. [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md).) [Bakım görevlileri ve çalışan gruplarındaki](../setup-for-objects/workers-and-worker-groups.md) bir çalışanla ilgili işlem yapılacak yerleşim yoksa, **Varlıklarım** sekmesi kullanılamaz. 

6. **Bakım işi türü** alanında iş emri için bakım işi türünü seçin.

7. Gerekirse, **Bakım işi türü çeşidi** ve **İşlem**'i seçin.

8. Gerekirse, **Servis düzeyi** alanında iş emri hizmet düzeyini değiştirebilirsiniz.

9. İlgili alanlarda **Beklenen başlangıç** ve **Beklenen bitiş** tarihlerini seçin.

10. İş emri oluşturmak için **Tamam**'a tıklayın.

11. **Tüm iş emirleri** liste sayfasında, iş emrini gerektiği gibi düzenleyebilirsiniz.

Aaşağıdaki noktaları unutmayın:

- **Tüm iş emirleri** liste sayfasının ayrıntılar görünümünde **İş emri bakım işleri** hızlı sekmesinde satırlar ekleyerek, iş emrine birden çok varlık ekleyebilirsiniz. Bir varlıkta, yalnızca varlık için seçilen varlık türünde tanımlanan bakım işi türlerini seçebilirsiniz.  

- Bir iş emri üzerinde kullandıktan sonra bir varlık hizmet düzeyini veya varlık kritikliğini değiştirirseniz, iş emrindeki hizmet düzeyi veya kritiklik buna göre güncelleştirilmez. Hizmet düzeyleri ve kritiklikler hakkında daha fazla bilgi için bkz. [Varlık hizmet düzeyleri](../setup-for-objects/object-priorities.md) ve [Varlık kritiklik türleri](../setup-for-objects/object-criticalities.md).

- İş emrindeki kritiklik, iş emrine bir iş emri işi eklendiğinde veya silindiğinde yeniden hesaplanır.

- **Tüm iş emirleri** ayrıntılar görünümünde > **Başlık** sekmesinde > **Zamanlama** hızlı sekmesindeki **Sorumlu grup** veya **Sorumlu** alanında bir sorumlu bakım görevlisi grubu veya sorumlu bakım görevlisi seçebilirsiniz. İş emri etkinken bu ayarlar değiştirilebilir. Örneğin, iş emri yaşam döngüsü durumu değiştiğinde değiştirilebilirler. İş emri oluşturma sırasında yapılan otomatik seçim, **Sorumlu bakım görevlileri** sayfasındaki kurulumu temel alır. Bir iş emri oluşturduktan sonra iş emri işlerini ekler veya kaldırırsanız ve iş emrini güncelleştirdiğinizde **Sorumlu grup** ve **Sorumlu** alanı boşsa, Varlık Yönetimi kurulum formunda sorumlu bir bakım görevlisi grubu veya sorumlu bakım görevlisi için olası bir eşleşme arar. İş emrini güncelleştirdiğinizde **Sorumlu grup** veya **Sorumlu** alanı zaten ayarlanmış durumda ise, hiçbir değişiklik yapılmaz. Sorumlu bakım görevlileri ve görevli gruplarıyla ilgili daha fazla bilgi için bkz: [Sorumlu bakım görevlileri](../setup-for-maintenance-requests/responsible-workers.md).

- [Bakım durumu](../controlling-and-reporting/maintenance-status.md) sayfasından gelen ve tamamlanan iş emirleriyle ilgili iş yükünün özetini almak için hesaplama yapabilirsiniz.  

- **Tüm iş emirleri** sayfasının ayrıntılar görünümünde **Aatır ayrıntıları** hızlı sekmesinde, iş emri işinde seçilen varlık için coğrafi koordinatlar eklemek amacıyla **Enlem** ve **Boylam** alanlarını kullanabilirsiniz.  


## <a name="create-related-work-order"></a>İlgili iş emri oluştur

Var olan bir iş emriyle ilgili bir iş emri oluşturabilirsiniz. Bu özellik, örneğin birincil ve ikincil iş emirleriyle çalışmak istiyorsanız yararlıdır. Yeni bir iş emri, var olan bir iş emrinden alınan bir iş emri işine dayalıdır.

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ni seçin.

2. İlgili iş emri oluşturulacak iş emrini seçin.

3. Eylem Bölmesinde **İş emri** sekmesindeki **Yeni** grubunda **İlgili iş emri**'ni seçin.

4. **İlgili iş emri oluştur** iletişim kutusunda, **İş emri işi** alanında ilgili iş emri oluşturmak istediğiniz iş emri işini seçin.

5. **Bakım işi türü** alanında bakım işi türünü seçin.

6. **Bakım işi türü çeşidi** ve **Zanaat** alanlarında gerektiği şekilde ilgili bir bakım işi türü çeşidi ve zanaat seçin.

7. Bu iş emri, seçili iş emri için oluşturulan ilk ilgili iş emriyse, şu adımları izleyin:
    1. **Yeni iş emri** seçeneğini belirleyin.
    2. **İş emri türü** alanında bir iş emri türü seçin.
    3. **Açıklama** alanına bir açıklama girin.
    4. **Hizmet düzeyi** alanında iş emri hizmet düzeyini gereken şekilde değiştirin.
    5. **Beklenen başlangıç** ve **Beklenen bitiş** alanlarında, beklenen başlangıç ve bitiş tarihlerini seçin.
    6. **Tamam**'ı seçin. Yeni ilgili iş emri **Tüm iş emirleri** liste sayfasında gösterilir.  

8. Bu ilişkili iş emrini oluşturduğunuz iş emrinin zaten ilgili iş emirleri varsa, var olan bir ilgili iş emrine yeni bir iş emri işi eklemek için aşağıdaki adımları izleyin:
    1. **İlgili iş emrine ekle** seçeneğini belirleyin.
    2. **İş emri** alanında, yeni bir iş emri işi ekleyeceğiniz ilgili iş emrini seçin.
    3. **Hizmet düzeyi** alanında iş emri hizmet düzeyini gereken şekilde değiştirin.
    4. **Beklenen başlangıç** ve **Beklenen bitiş** alanlarında, beklenen başlangıç ve bitiş tarihlerini gereken şekilde değiştirin.
    5. **Tamam**'ı seçin. İş emri işi var olan ilgili iş emrine eklenir.

Aşağıdaki şekilde **İlgili iş emri oluştur** iletişim kutusu örneği gösterilmektedir.

![Şekil 1](media/03-work-orders.png)

>[!NOTE]
>**Varlık yönetimi parametreleri** > **İş emirleri** sekmesi > **İlgili iş emri maskesi** alanında ilgili iş emri maskesi ayarlarsanız, iş emri kodları maske ayarına uygun şekilde oluşturulur. İlgili bir iş emri maskesi ayarlanmamışsa, ilgili iş emirleri için sonraki kullanılabilir iş emri kodu kullanılır.

## <a name="copy-a-work-order"></a>İş emri kopyalama

Var olan bir iş emrinden hızlı şekilde yeni bir iş emri oluşturabilirsiniz. İş emirleriyle çalışmanın bu yolu, [bakım planlarını](../preventive-and-reactive-maintenance/maintenance-plans.md) temel alan iş emirleri oluşturmaktan farklıdır. Örneğin, farklı varlıklarda düzenli aralıklarla tamamlanması gereken çeşitli işler içeren birçok iş emri işi bulunan bir iş emri varsa yararlıdır.

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ni seçin.

2. İçeriği kopyalamak istediğiniz iş emrini seçin.

3. Eylem Bölmesinde >**İş emri** sekmesinde > **Yeni** grubunda **İş emrini kopyala**'yı seçin.

4. Seçilen iş emrinden alınan iş emri kurulumu görüntülenir. Alanların bazılarını istediğiniz şekilde düzenleyebilirsiniz.

5. Yeni iş emri oluşturmak için **Tamam**'ı seçin.

6. **Tüm iş emirleri** liste sayfasında, iş emrini gerektiği gibi düzenleyebilirsiniz.

>[!NOTE]
>Yeni iş emri oluşturulduğunda, bazı bilgiler doğrudan var olan iş emrinden kopyalanır. Tahminler, araçlar, bakım denetim listeleri, işlem yapılacak yerleşim, adresler ve zamanlama hakkındaki bilgiler kopyalanmaz. Bunun yerine, Varlık Yönetiminde geçerli kurulumdan başlatılır. Bu nedenle, ilk iş emrinin oluşturulduğu zaman ile iş emrinin kopyasını oluşturduğunuz zaman arasında bilgiler değiştirilirse, değişiklikler yeni iş emrine dahil edilir. Örnekler tahminlerdeki değişiklikleri veya bakım denetim listelerindeki güncelleştirmelerdir.

Aşağıdaki örnekte **İş emrini kopyala** iletişim kutusunun bir örneği gösterilmektedir.

![Şekil 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a>Bakım isteğine dayalı iş emri oluşturma

1. **Varlık yönetimi** > **Ortak** > **Bakım talepleri** > **Tüm bakım talepleri** ya da **Etkin bakım talepleri**'ni seçin.

2. İş emri oluşturmak istediğiniz bakım talebini seçin ve **Düzenle**'ye tıklayın.

3. Eylem Bölmesinde >**Bakım talebi** sekmesinde > **Yeni** grubunda **İş emri**'ni seçin.

4. **İş emri** iletişim kutusunda, alanları ayarlayın. Bakım talebinde bir bakım işi türü seçilmişse, iş emrini oluştururken gerekirse farklı bir bakım işi türü seçebilirsiniz.

5. **Tamam**'ı seçin. Bir ileti, bir satış siparişinin oluşturulduğunu bildirir.

6. Bir bakım talebine bağlı iş emirlerini görüntülemek için **Tüm bakım talepleri** veya **Etkin bakım talepleri** liste sayfasında bakım talebini seçin. Ardında Eylem Bölmesinde **Bakım talebi** sekmesinde **Görüntüle** grubunda **İş emirleri**'ni seçin.


Aşağıdaki çizimde **İş emri oluştur** iletişim kutusunun bir örneği gösterilmektedir.

![Şekil 3](media/05-work-orders.png)


>[!NOTE]
>İş emirlerinin otomatik oluşturulmasını isterseniz, bakım planı işlerini planlayabilir veya bir varlıkta [bakım planlarını](../preventive-and-reactive-maintenance/maintenance-plans.md) veya [bakım sıralarını](../preventive-and-reactive-maintenance/maintenance-rounds.md) "otomatik oluştur" özelliğini ayarlayabilirsiniz. **Tüm bakım zamanlamaları** liste sayfasındaki bakım taleplerinden oluşturulan iş emirleri, bakım taleplerinde seçilen bakım işi türlerine sahiptir.

