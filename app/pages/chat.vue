<template>
  <ChatWindow :typing :chat :messages @send-message="handleSendMessage" />
</template>

<script setup>
const { chat, messages, sendMessage } = useChat();
const typing = ref(false);

const handleSendMessage = async (message) => {
  typing.value = true;
  await sendMessage(message);
  typing.value = false;
};
const appconfig = useAppConfig();
const title = computed(() =>
  chat.value?.title ? `${chat.value.title}-${appconfig.title}` : appconfig.title
);
useHead({
  title,
});
</script>

<style lang="scss" scoped></style>
