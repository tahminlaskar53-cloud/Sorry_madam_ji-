# Sorry_madam_ji-
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>A Little Message</title>

    <style>
        body {
            margin: 0;
            height: 100vh;
            background: #fff0f5;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: Georgia, serif;
        }

        .container {
            width: 90%;
            max-width: 350px;
            text-align: center;
        }

        .title {
            font-size: 25px;
            color: #5a3d4a;
            margin-bottom: 25px;
        }

        .card {
            background: white;
            border-radius: 18px;
            padding: 30px 25px;
            min-height: 260px;
            box-shadow: 0 8px 25px rgba(90, 61, 74, 0.12);

            display: flex;
            justify-content: center;
            align-items: center;
        }

        .message {
            color: #4a3940;
            font-size: 16px;
            line-height: 1.7;
        }

        .hint {
            margin-top: 20px;
            color: #8a6f7a;
            font-size: 13px;
        }

        .page-number {
            margin-top: 12px;
            color: #8a6f7a;
            font-size: 12px;
        }

        .special {
            font-size: 19px;
            font-style: italic;
            line-height: 1.8;
        }

        .love {
            margin-top: 25px;
            font-size: 28px;
            color: #5a3d4a;
            font-style: italic;
        }
    </style>
</head>

<body>

<div class="container">

    <div class="title" id="title">
        Hey Madam Ji :)
    </div>

    <div class="card" id="card">

        <div class="message" id="message">
            Akansha, I made something for you.
            I know it's not perfect,
            but I really hope tumhe pasand aaye.

            <br><br>

            Bas kuch baatein thi jo mujhe
            properly bolni thi...
        </div>

    </div>

    <div class="hint" id="hint">
        Swipe to continue
    </div>

    <div class="page-number" id="pageNumber">
        1 / 4
    </div>

</div>


<script>

let currentPage = 0;

const pages = [

    {
        title: "Hey Madam Ji :)",
        message: `
            Akansha, I made something for you.
            I know it's not perfect,
            but I really hope tumhe pasand aaye.

            <br><br>

            Bas kuch baatein thi jo mujhe
            properly bolni thi...
        `
    },

    {
        title: "Okay Madam Ji, Sorry",
        message: `
            Mujhe laga tum mujhse pyaar nahi karti,
            aur jab tum reply nahi kar rahi thi,
            to mujhe laga shayad mujhe bhi
            tumse zyada baat nahi karni chahiye.

            <br><br>

            But maybe... main galat tha.

            <br><br>

            Shayad maine tumpe thoda zyada
            hi shak kar liya.

            <br><br>

            And I'm really sorry for that.
        `
    },

    {
        title: "Meri Overthinking",
        message: `
            Main na cheezon ko lekar thoda
            zyada overthink karta hoon.

            <br><br>

            Iss baar bhi maine shayad
            zarurat se zyada soch liya.

            <br><br>

            Ab mujhe realize ho raha hai ki
            shayad main hi galat tha.

            <br><br>

            I'm really, really sorry,
            Madam Ji.
        `
    },

    {
        title: "Bas Ek Baat",
        message: `
            <div class="special">

                In sab ke liye I'm really sorry.

                <br><br>

                Mujhe maaf kar do na,
                Madam Ji.

                <br><br>

                Aur agar tum comfortable ho,
                toh mujhse phir se baat kar lena.

                <br><br>

                I'm sorry, Akansha.

                <div class="love">
                    I Love You
                </div>

            </div>
        `
    }

];


function showPage() {

    document.getElementById("title").innerHTML =
        pages[currentPage].title;

    document.getElementById("message").innerHTML =
        pages[currentPage].message;

    document.getElementById("pageNumber").innerHTML =
        (currentPage + 1) + " / " + pages.length;

}


let startX = 0;

document.addEventListener("touchstart", function(event) {

    startX = event.touches[0].clientX;

});


document.addEventListener("touchend", function(event) {

    let endX = event.changedTouches[0].clientX;

    let distance = endX - startX;


    if (distance < -50 && currentPage < pages.length - 1) {

        currentPage++;
        showPage();

    }


    if (distance > 50 && currentPage > 0) {

        currentPage--;
        showPage();

    }

});


</script>

</body>
</html>
