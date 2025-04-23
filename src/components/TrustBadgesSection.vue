<template>
  <q-card class="q-my-md no-shadow bg-white" bordered>
    <q-card flat bordered class="q-pa-md">
      <trust-badge
        icon="check_circle"
        title="Safe payments"
        description="Shop confidently with our secure payment options. All card details are encrypted for maximum protection during transactions."
      >
        <div class="q-pl-lg row q-mb-lg q-gutter-lg">
          <payment-card-image v-for="(card, index) in paymentCards" :key="index" :src="card" />
        </div>
      </trust-badge>

      <div class="text-grey-7 w-full q-mb-md border-light" />

      <trust-badge
        icon="lock"
        title="Secure policy"
        description="Your privacy matters to us. We guarantee that your personal information will never be shared with third parties."
      />

      <trust-badge
        icon="phone"
        title="Dedicated support"
        description="Need help? Our dedicated support team is available by phone to assist with any questions or issues you may have."
      />
    </q-card>
  </q-card>
</template>

<script setup lang="ts">
import TrustBadge from './TrustBadge.vue';
import PaymentCardImage from './PaymentCardImage.vue';

const paymentCards: string[] = [
  'https://raw.githubusercontent.com/datatrans/payment-logos/master/assets/cards/visa.svg',
  'https://raw.githubusercontent.com/datatrans/payment-logos/master/assets/cards/mastercard.svg',
  'https://raw.githubusercontent.com/datatrans/payment-logos/master/assets/cards/discover.svg',
  'https://raw.githubusercontent.com/datatrans/payment-logos/master/assets/wallets/apple-pay.svg',
  'https://raw.githubusercontent.com/datatrans/payment-logos/master/assets/wallets/google-pay.svg',
];
</script>
