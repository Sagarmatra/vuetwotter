
<template>
    <div class="twoot-item">
        <div class="user-profile__twoot">
            <div class="twoot-item__user">
                @{{ username }}
            </div>
            <div class="twoot-item__content">
                {{ twoot. content }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Twoot",
    props: {
        username: {
            type: String,
            required: true,
        },
        twoot: {
            type: Object,
            required: true,
        }
    }
};
</script>

<style lang="scss" scoped>
.twoot-item {
    padding: 15px 15px 15px 15px;
    margin: 5px 0;
    background-color: white;
    border-radius: 5px;
    border: 1px solid #DFE3E8;
    box-sizing: border-box;
    cursor: pointer;
    transition: all 0.25s ease;

    &:hover {
    transform: scale(1.09, 1.1);
    }

    .twoot-item__user {
    font-weight: bold;
    }

    .twoot-item__content {
        margin-top: 5px;
    }
}

.twoot-item:first-of-type {
    margin-top: 0;
}



</style>