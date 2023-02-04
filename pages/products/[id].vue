<template>
  <div>
    <ProductDetails :product="product" />
  </div>
</template>

<script setup>
const { id } = useRoute().params;

//data fetch
const { data: product } = await useFetch(
  `https://fakestoreapi.com/products/${id}`
);

//throw error if product is empty
if (!product.value) {
  throw createError({
    statusCode: 404,
    message: "Product not found",
    fatal: true,
  });
  //(fata: true) this will show the error page  when routing to a product/id that does not exist ((client side)) if we are not fetching from backend
}
</script>

<style scoped></style>
