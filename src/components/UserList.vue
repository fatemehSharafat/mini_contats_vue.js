<template >
  <div class="box2">
    <!-- box2 row1-->
    <div class="row justify-content-center">
      <!-- photo-->
      <div class="col-2">
        <img
          class="img img-sm"
          id="photo1"
          src="./ac1.png"
          alt="logo"
          style="max-width: 62px"
        />
      </div>
      <!-- name & wname-->
      <div class="col-4 mt-2">
        <!-- name -->
        <div class="row justify-content-right">
          <p class="fon pb-0 mb-0">در جاده نيست</p>
        </div>
        <!-- wname -->
        <div class="row justify-content-right pt-0 mt-0">
          <p>زرين بار</p>
        </div>
      </div>
      <!-- call btn-->
      <div class="col-3 mt-4">
        <button
          type="button"
          class="btn btn-sm btn-responsive btn-outline-success w-100"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-telephone-fill"
            viewBox="0 0 16 16"
          >
            <path
              fill-rule="evenodd"
              d="M1.885.511a1.745 1.745 0 0 1 2.61.163L6.29 2.98c.329.423.445.974.315 1.494l-.547 2.19a.678.678 0 0 0 .178.643l2.457 2.457a.678.678 0 0 0 .644.178l2.189-.547a1.745 1.745 0 0 1 1.494.315l2.306 1.794c.829.645.905 1.87.163 2.611l-1.034 1.034c-.74.74-1.846 1.065-2.877.702a18.634 18.634 0 0 1-7.01-4.42 18.634 18.634 0 0 1-4.42-7.009c-.362-1.03-.037-2.137.703-2.877L1.885.511z"
            />
          </svg>
          تماس
        </button>
      </div>
      <!-- delete btn-->
      <div class="col-3 mt-4">
        <button
          type="button"
          class="btn btn-sm btn-responsive btn-outline-danger w-100"
          @click="deleteItem(item)"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-archive-fill"
            viewBox="0 0 16 16"
          >
            <path
              d="M12.643 15C13.979 15 15 13.845 15 12.5V5H1v7.5C1 13.845 2.021 15 3.357 15h9.286zM5.5 7h5a.5.5 0 0 1 0 1h-5a.5.5 0 0 1 0-1zM.8 1a.8.8 0 0 0-.8.8V3a.8.8 0 0 0 .8.8h14.4A.8.8 0 0 0 16 3V1.8a.8.8 0 0 0-.8-.8H.8z"
            />
          </svg>
          حذف
        </button>
      </div>
    </div>

    <hr />

    <!-- box2 row2-->
    <div class="row justify-content-right">
      <!-- car -->
      <div class="col-4">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="16"
          height="16"
          fill="currentColor"
          class="bi bi-car-front-fill"
          viewBox="0 0 16 16"
        >
          <path
            d="M2.52 3.515A2.5 2.5 0 0 1 4.82 2h6.362c1 0 1.904.596 2.298 1.515l.792 1.848c.075.175.21.319.38.404.5.25.855.715.965 1.262l.335 1.679c.033.161.049.325.049.49v.413c0 .814-.39 1.543-1 1.997V13.5a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1-.5-.5v-1.338c-1.292.048-2.745.088-4 .088s-2.708-.04-4-.088V13.5a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1-.5-.5v-1.892c-.61-.454-1-1.183-1-1.997v-.413a2.5 2.5 0 0 1 .049-.49l.335-1.68c.11-.546.465-1.012.964-1.261a.807.807 0 0 0 .381-.404l.792-1.848ZM3 10a1 1 0 1 0 0-2 1 1 0 0 0 0 2Zm10 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2ZM6 8a1 1 0 0 0 0 2h4a1 1 0 1 0 0-2H6ZM2.906 5.189a.51.51 0 0 0 .497.731c.91-.073 3.35-.17 4.597-.17 1.247 0 3.688.097 4.597.17a.51.51 0 0 0 .497-.731l-.956-1.913A.5.5 0 0 0 11.691 3H4.309a.5.5 0 0 0-.447.276L2.906 5.19Z"
          />
        </svg>
        <p class="d-inline">تريلي كفي</p>
      </div>
      <!-- location-->
      <div class="col-4">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="16"
          height="16"
          fill="currentColor"
          class="bi bi-geo-alt-fill"
          viewBox="0 0 16 16"
        >
          <path
            d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10zm0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6z"
          />
        </svg>
        <p class="d-inline">تهران- تهران</p>
      </div>
      <!-- number-->
      <div class="col-4">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="16"
          height="16"
          fill="currentColor"
          class="bi bi-telephone-fill"
          viewBox="0 0 16 16"
        >
          <path
            fill-rule="evenodd"
            d="M1.885.511a1.745 1.745 0 0 1 2.61.163L6.29 2.98c.329.423.445.974.315 1.494l-.547 2.19a.678.678 0 0 0 .178.643l2.457 2.457a.678.678 0 0 0 .644.178l2.189-.547a1.745 1.745 0 0 1 1.494.315l2.306 1.794c.829.645.905 1.87.163 2.611l-1.034 1.034c-.74.74-1.846 1.065-2.877.702a18.634 18.634 0 0 1-7.01-4.42 18.634 18.634 0 0 1-4.42-7.009c-.362-1.03-.037-2.137.703-2.877L1.885.511z"
          />
        </svg>
        <p class="d-inline">{{ item.pnum }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["item"],
  methods: {
    deleteItem(item) {
      this.$emit("delete-item", item);
    },
  },
};
</script>

<style>
div.box2 {
  background: white;
  padding: 20px;
  border-radius: 19px;
  box-shadow: 1px 1px 9px #dedddd;
  margin-top: 7px;
}
#photo1 {
  border-radius: 40px;
}
.fon {
  font-weight: bold;
}
</style>