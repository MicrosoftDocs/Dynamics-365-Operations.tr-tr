---
title: Satış siparişi durumu sütunları için eşlemeyi ayarlama
description: Bu konu, çift yazma için satış siparişi durumu sütunlarının nasıl ayarlanacağını açıklar.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: damadipa
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 53d824ca2fb1eadf34e62bf9c08b837db3efaf42
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782296"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>Satış siparişi durumu sütunları için eşlemeyi ayarlama

[!include [banner](../../includes/banner.md)]

Satış siparişi durumunu gösteren sütunlar, Microsoft Dynamics 365 Supply Chain Management ve Dynamics 365 Sales uygulamalarında farklı sabit numaralandırma değerlerine sahiptir. Bu sütunları çift-yazılır olarak eşlemek için ek kurulum gerekir.

## <a name="columns-in-supply-chain-management"></a>Supply Chain Management'ta sütunlar

Supply Chain Management'ta, iki sütun satış siparişinin durumunu yansıtır. Eşlemeniz gereken sütunlar **Durum** ve **Belge Durumu** sütunlarıdır.

**Durum** numaralandırma alanı siparişin genel durumunu belirtir. Bu durum sipariş başlığında gösterilir.

**Durum** numaralandırma alanında aşağıdaki değerler bulunur:

- Açık Sipariş
- Teslim edildi
- Faturalanan
- İptal edildi

**Belge Durumu** numaralandırma alanı sipariş için oluşturulan en son belgeyi belirtir. Örneğin, sipariş onaylandığında bu belge bir satış siparişi onayıdır. Bir satış siparişi kısmen faturalanmışsa ve kalan satır onaylandıysa, belge durumu **Fatura** olarak kalır, çünkü fatura bu işlem içinde daha sonra oluşturulmuştur.

**Belge Durumu** numaralandırma alanında aşağıdaki değerler bulunur:

- Onay
- Malzeme Çekme Listesi
- Sevk İrsaliyesi
- Fatura

## <a name="columns-in-sales"></a>Sales'da sütunlar

Sales'da, iki sütun siparişin durumunu yansıtır. Eşlemeniz gereken sütunlar **Durum** ve **İşleme Durumu** sütunlarıdır.

**Durum** numaralandırma alanı siparişin genel durumunu belirtir. Aşağıdaki değerlere sahiptir:

- Active
- Gönderildi
- Yerine getirildi
- Faturalanan
- İptal edildi

**İşlem Durumu** numaralandırma alanı, Supply Chain Management ile daha doğru şekilde eşleştirilebilecek şekilde kullanılmaya başlandı.

Aşağıdaki tablo, Supply Chain Management uygulamasında **İşleme Durumu** alanlarının eşlemesini gösterir.

| İşlem Durumu   | Supply Chain Management'ta durum | Supply Chain Management'ta Belge Durumu |
|---------------------|-----------------------------------|--------------------------------------------|
| Active              | Açık Sipariş                        | Hiçbiri                                       |
| Onaylı           | Açık Sipariş                        | Onay                               |
| Çekildi              | Açık Sipariş                        | Malzeme Çekme Listesi                               |
| Kısmen Teslim Edildi | Açık Sipariş                        | Sevk İrsaliyesi                               |
| Teslim edildi           | Teslim edildi                         | Sevk İrsaliyesi                               |
| Kısmen Faturalandı  | Teslim edildi                         | Fatura                                    |
| Faturalanan            | Faturalanan                          | Fatura                                    |
| İptal edildi           | İptal edildi                         | Geçerli değil                             |

Aşağıdaki tablo, Sales ile Supply Chain Management uygulamaları arasında **İşleme Durumu** alanlarının eşlemesini gösterir.

| İşlem Durumu   | Sales'ta Durum | Supply Chain Management'ta durum |
|---------------------|-----------------|-----------------------------------|
| Active              | Active          | Açık Sipariş                        |
| Onaylı           | Gönderildi       | Açık Sipariş                        |
| Çekildi              | Gönderildi       | Açık Sipariş                        |
| Kısmen Teslim Edildi | Active          | Açık Sipariş                        |
| Kısmen Faturalandı  | Active          | Açık Sipariş                        |
| Kısmen Faturalandı  | Yerine getirildi       | Teslim edildi                         |
| Faturalanan            | Faturalanan        | Faturalanan                          |
| İptal edildi           | İptal edildi       | İptal edildi                         |

## <a name="setup"></a>Ayar

Satış siparişi durumu sütunlarıyla ilgili eşlemeyi ayarlamak için **IsSOPIntegrationEnabled** ve **isIntegrationUser** özniteliklerini etkinleştirmelisiniz.

**IsSOPIntegrationEnabled** özniteliğini etkinleştirmek için şu adımları izleyin.

1. Web tarayıcısında `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations` adresine gidin. **\<test-name\>** değerini şirketinizin Sales bağlantısı ile değiştirin.
2. Açılan sayfada, **organizationId** değerini bulun ve değeri not alın.

    ![organizationId bulma.](media/sales-map-orgid.png)

3. Sales'ta, tarayıcı konsolunu açın ve aşağıdaki kodu çalıştırın. 2. adımdaki **organizationId** değerini kullanın.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![Tarayıcı konsolundaki JavaScript kodu.](media/sales-map-script.png)

4. **IsSOPIntegrationEnabled** değerinin **TRUE** olarak ayarlandığını doğrulayın. Değeri kontrol etmek için 1. adımdaki URL'yi kullanın.

    ![IsSOPIntegrationEnabled değeri doğru olarak ayarlanmış.](media/sales-map-integration-enabled.png)

**isIntegrationUser** özniteliğini etkinleştirmek için şu adımları izleyin.

1. Sales'da, **Ayarlar \> Özelleştirme \> Sistemi Özelleştirme** sayfasına gidin, **Kullanıcı tablosu** ögesini seçin ve sonra **Form \> Kullanıcısı** ögesini açın.

    ![Kullanıcı formunu açma.](media/sales-map-user.png)

2. Alan Gezgini'nde, **Tümleştirme kullanıcısı modunu** bulun ve forma eklemek için çift tıklayın. Değişikliğinizi kaydedin.

    ![Tümleştirme kullanıcısı modu sütununu forma ekleme.](media/sales-map-field-explorer.png)

3. Sales'ta, **Ayarlar \> Güvenlik \> Kullanıcılar** sayfasına gidin ve görünümü **Etkin Kullanıcılar** ayarından **Uygulama kullanıcıları** olarak değiştirin.

    ![Görünümü Etkin Kullanıcılardan Uygulama Kullanıcıları olarak değiştirme.](media/sales-map-enabled-users.png)

4. **DualWrite IntegrationUser** için iki giriş seçin.

    ![Uygulama kullanıcıları listesi.](media/sales-map-user-mode.png)

5. **Tümleştirme kullanıcısı modu** sütununun değerini **Evet** olarak değiştirin.

    ![Tümleştirme kullanıcısı modu sütununun değerini Evet olarak değiştirme.](media/sales-map-user-mode-yes.png)

Satış siparişleriniz artık eşlendi.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]