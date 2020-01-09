## Miscelanius


Search for the text customer/{any text}/paymentcards
    rg 'customer/\{.*\}/paymentcards'



git grep 'customer/.*/paymentcards' $(git rev-list --all -- /F/source/icenet-applications/icenet-domain/Web/API/IceNet.Api/Controllers/EntityPaymentCardController.cs) -- /F/source/icenet-applications/icenet-domain/Web/API/IceNet.Api/Controllers/EntityPaymentCardController.cs