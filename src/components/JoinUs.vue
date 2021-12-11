<template>
    <section class="join-us py-5 mt-5">
        <SectionTitle class="w-50 mx-auto mt-5"
            title="Change a life today"
            subtitle="As long as poverty, injustice & inequality persist, none of us can truly rest. It doesn't take much to change a life. get in touch today and start making the difference."
            position="center"
        />
        <div class="actions text-center mt-5">
            <BtnBordered class="me-3"
                text="Volunteer"
            />
            <BtnBordered 
                text="Donate Now"
            />
        </div>
    </section>
</template>

<script>
import SectionTitle from '@/components/SectionTitle.vue'
import BtnBordered from '@/components/BtnBordered.vue'
export default {
    name: 'JoinUs',
    components: {
        SectionTitle,
        BtnBordered,
    }
}
</script>

<style scoped lang="scss">
    .join-us {
        min-height: 450px;
        color: white;
        background-image: url('../assets/home-footer.jpg');
        background-position: center;
        background-size: cover;
        a.ms-btn {
            border: 2px solid currentColor;
        }
    }
</style>