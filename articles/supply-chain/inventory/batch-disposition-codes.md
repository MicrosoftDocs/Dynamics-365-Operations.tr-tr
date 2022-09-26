---
title: Kullanılabilir veya kullanılamayan olarak toplu işleri işaretlemek için toplu iş değerlendirme kodlarını kullan
description: Bu makalede, kullanılabilir veya kullanılamayan ana planlama, rezervasyon, malzeme çekme ve/veya sevkiyatta kullanıma hazır toplu işleri işaretlemek için toplu iş değerlendirme kodlarının nasıl ayarlanacağı ve kullanılacağı açıklanır.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542480"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Kullanılabilir veya kullanılamayan olarak toplu işleri işaretlemek için toplu iş değerlendirme kodlarını kullan

Bu makalede, *toplu dağıtım kodlarının* nasıl kurulacağı ve kullanılacağı açıklanmaktadır. Her toplu iş dağıtım kodunun durumu *Kullanılabilir* veya *Kullanılamaz* durumda olabilir. Her toplu işin ana planlama, rezervasyon, malzeme çekme ve/veya sevkiyat için kullanılabilir olup olmadığını göstermek üzere stok toplu işlemlerine toplu iş değerlendirme kodları atarsınız.

Toplu iş değerlendirme kodlarını kullanmak için kodları ayarlamanız ve bunları yönetmek istediğiniz toplu işlerle atamanız gerekir.

## <a name="set-up-batch-disposition-codes"></a>Toplu iş değerlendirme kodlarını ayarla

Sisteminizde kullanmak istediğiniz toplu iş değerlendirme kodunu ayarlamanız gerekir. İstediğiniz sayıda kod oluşturabilirsiniz. (Örneğin, bir toplu işin kullanılabilir veya kullanılamaz olma olasılığı olan farklı nedenleri tanımlamak için kodlar oluşturabilirsiniz). Ancak, genellikle şu iki kodu elde edebilirsiniz: biri *kullanılabilir* durumda ve diğeri *kullanılamıyor*. Ayrıca, bir toplu işin bazı operasyonlar için kullanılmasına olanak tanıyan özel kodlar da oluşturabilirsiniz.

Toplu iş değerlendirme kodları oluşturmak için bu adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Toplu iş \> Toplu iş değerlendirme ana**'ya gidin.
1. **Toplu iş değerlendirme ana** sayfası, geçerli toplu iş değerlendirme kodlarınızı listeler ve bunları oluşturmanızı, silmenizi ve düzenlemenizi sağlar. Şu adımlardan birini izleyin:

    - Varolan bir kodu düzenlemek için, birimi liste bölmesinde seçin.
    - Yeni bir kod oluşturmak için Eylem Bölmesinde **Yeni**'yi seçin.

1. Yeni veya seçili kodun üst bilgisinde aşağıdaki alanları ayarlayın:

    - **Toplu iş değerlendirme kodu** – Kodun görünen adını girin.
    - **Açıklama** – Kodun nasıl kullanılması gerektiğini açıklayın.
    - **Toplu iş değerlendirme durumu** – Kodun atandığı toplu işler için geçerli olan durumu seçin.

        - *Kullanılamaz* – Toplu işler ana planlama, rezervasyon, çekme veya sevkiyat için kullanılamaz. Bu değeri seçtiğinizde, **Kurulum** hızlı sekmesindeki tüm **Engelle** seçenekleri *Evet* olarak ayarlanır ve **Netleştirilebilir** seçenekleri *Hayır* olarak ayarlanır. Ancak, özel durum eklemek için bu ayarlardan bazılarını değiştirebilirsiniz.
        - *Kullanılabilir* – Toplu işler ana planlama, rezervasyon, çekme ve/veya sevkiyat için kullanılabilir. Bu değeri seçtiğinizde, **Kurulum** hızlı sekmesindeki tüm **Engelle** seçenekleri *Hayır* olarak ayarlanır ve **Netleştirilebilir** seçenekleri *Evet* olarak ayarlanır. Bu ayarlar, **Toplu iş değerlendirme durumu** alanı *Kullanılabilir* olarak ayarlandığında salt okunur olur.

1. **Toplu iş değerlendirme durumu** alanını *Kullanılamaz* olarak ayarlarsanız, her sipariş türü (satış, transfer ve üretim) için her operasyonun bloke durumunu (rezerve et, çek ve sevk et) özelleştirebilirsiniz. Üretim emirleri için, üretim malzeme çekme günlüğünün bloke etmeyi veya engelini kaldırmayı seçebilirsiniz. Ayrıca, ana planlamayı bloke etmeyi veya engelini kaldırmayı da seçebilirsiniz. Her bir işlemi gereksinim duyduğunuz şekilde engellemek veya engelini kaldırmak için **Kurulum** hızlı sekmesindeki seçenekleri kullanın. Ana planlamayı etkinleştirmek için **Netleştirilebilir** seçeneğini *Evet* olarak ayarlayın veya ana planlamayı engellemek için *Hayır* olarak ayarlayın.

## <a name="assign-batch-disposition-codes-to-batches"></a>Toplu iş değerlendirme kodlarını toplu işlere atama

Gereksinim duyduğunuz toplu iş değerlendirme kodlarını tanımladıktan sonra, bunları toplu işlemlere atamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Stok \> Toplu işler** seçeneğine gidin.
1. Bir toplu iş değerlendirme kodu atamak için bir veya daha fazla toplu iş seçin.
1. Eylem Bölmesi'ndeki **Sıfırla** sekmesinde, **Toplu iş değerlendirme kodunu sıfırla**'yı seçin.
1. **Stok toplu işindeki sınırlamaları değiştir** iletişim kutusunda, **Yeni toplu iş değerlendirme kodu** alanını atamak istediğiniz kodun adı olarak ayarlayın.
1. Yeni ayarı uygulayıp değişikliğinizi kaydetmek için **Tamam**'ı seçin.

    **Toplu işler** sayfasında, **Toplu iş değerlendirme kodu** ve **Toplu iş değerlendirme durumu** sütunlarındaki değerler, seçili toplu işlerle ilgili ayarları yansıtacak şekilde güncelleştirilir.

## <a name="master-planning-example"></a>Master planlama örneği

Bu örnek toplu iş değerlendirme kodlarının ana planlamayı nasıl etkileyebileceğini gösterir.

Bu örnekte toplu değerlendirme kodları aşağıdaki şekilde ayarlanır:

- *P-Kullanılabilir:*

    - **Toplu iş değerlendirme durumu:** *Kullanılabilir*
    - **Netleştirilebilir:** *Evet*

- *P-Kullanılamaz:*

    - **Toplu iş değerlendirme durumu:** *Kullanılamaz*
    - **Netleştirilebilir:** *Hayır*

İki toplu işlem içeren bir ürün (*Ürün-1*) vardır: *Toplu İş-A* ve *Toplu İş-B* Bu toplu işler aşağıdaki şekilde ayarlanır:

- *Toplu İş-A:*

    - **Toplu iş değerlendirme kodu:** *P-Kullanılabilir*
    - **Eldeki miktar:** 1

- *Toplu İş-B*

    - **Toplu iş değerlendirme kodu:** *P-Kullanılamaz*
    - **Eldeki miktar:** 1

*Ürün-1* ürününden miktar olarak 2 adet için bir satış siparişi vardır (*SO1*). Teslimat tarihi bugünden itibaren üç gün.

Ana planlama çalıştırabilir ve bu örnekle ilgili aşağıdaki değerleri ayarlayabilirsiniz:

- **Planlanan sipariş:** *Satınalma siparişi*
- **Stok yenileme stratejisi:** *Gereksinim*
- **Sağlama süresi:** *0*

Planlama çalışması sonucunda, sistem, satış siparişi *SO1* için 1 ürün *Ürün-1* miktarını kapsamak üzere kullanılabilir toplu işi (*Toplu İş-A*) kullanır. Ancak, toplu iş *Toplu İş-B*'yi kullanılamaz, çünkü bu grup, planlama için uygun değil olarak işaretlendi. Bu nedenle, kalan miktarı karşılamak için, sistem yeni bir *Ürün-1* ürünü için planlı bir satınalma siparişi (*PPO1*) oluşturur.

Aşağıdaki çizim, planlanan sonuç zaman çizelgesini gösterir.

![Toplu iş değerlendirme kodlarının ana planlamayı nasıl etkileyebileceğini gösteren örnek.](media/batch-codes-planning-example.png "Toplu iş değerlendirme kodlarının ana planlamayı nasıl etkileyebileceğini gösteren örnek")
