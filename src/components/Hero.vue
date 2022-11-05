<template>
    <div class="hero">
        <div class="col">
            <h1>Bring everyone together to build better products.</h1>
            <p>Manage makes it simple for software teams to plain 
                day-to-day tasks while keeping the larger team goals in view</p>
            <button type="submit">Get Started</button>
        </div>
        <div class="col">
            <img src="images/illustration-intro.svg" alt="Illustration">
        </div>
    </div>
    <div class="hero">
        <div class="col manage">
            <h1>What's different about Manage?</h1>
            <p>Manage provides all the functionality your team needs, without
               the complexity. Our software is tailor-made for modern digital product teams.
            </p>
        </div>
        <div class="col about">
            <div class="row">
                <div>
                    <p>01</p>
                </div>
                <div>
                    <p>Track company-wide progress</p>
                    <p>See how your day-to-day tasks fit into the wider vision.
                        Go from tracking progress at the milestone level all the way done 
                        to the smallest of details. Never lose sight of the bigger picture 
                        again.
                    </p>
                </div>
            </div>
            <div class="row">
                <div>
                    <p>02</p>
                </div>
                <div>
                    <p>Advanced built-in reports</p>
                    <p>Set internal delivery estimates and track progress toward company
                        goals. Our customisable dashbaord helps you build out the reports
                        you need to keep key stakeholders informed.
                    </p>
                </div>
            </div>
            <div class="row">
                <div>
                    <p>03</p>
                </div>
                <div>
                    <p>Everything you need in one place</p>
                    <p>Stop jumping from one service to another to communicate, store files, track tasks
                        and share documents. Manage offers on all-in-one team productivity solution.
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Hero"
}
</script>

<style lang="scss" scoped>
@import "../css/__colors.scss";
@import "../css/__fonts.scss";

.hero{
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-wrap: wrap;
}

.col{
    padding: 2em;
    width: 30em;

    p{
        color: map-get($colors , dark-grayish-blue );
        margin-bottom: 30px;
        font-family: "Be Vietnam", sans-serif;
        text-align: left;
        width: 22.5em;
    }
}

.col:nth-of-type(2){
    width: 40em;
    padding: 1em!important;
}

.manage{
    align-self: flex-start;

    h1{
        font-size: 2em;
    }
}

.about{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;

    .row{
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .row div:nth-of-type(1){
        align-self: flex-start;
        margin-right: 30px;

        p{
        border-radius: 20px;
        width: 4rem!important;
        padding: 0.3rem 0.5rem;
        text-align: center;
        background-color: map-get($colors , bright-red );
        color: map-get($colors , very-light-gray );
        }
    }

    .row div:nth-of-type(2) p:nth-of-type(1){
        color: map-get($colors , dark-blue );
        font-weight: 500;
    }
}
</style>