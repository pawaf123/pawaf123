var wrapper = document.getElementsByClassName("xb57i2i x1q594ok x5lxg6s x78zum5 xdt5ytf x6ikm8r x1ja2u2z x1pq812k x1rohswg xfk6m8 x1yqm8si xjx87ck xx8ngbg xwo3gff x1n2onr6 x1oyok0e x1odjw0f x1iyjqo2 xy5w88m");
var list = wrapper[0].getElementsByClassName("x1i10hfl xjbqb8w x6umtig x1b1mbwd xaqea5y xav7gou x1ypdohk xe8uvvx xdj266r x11i5rnm xat24cr x1mh8g0r xexx8yu x4uap5 x18d9i69 xkhd6sd x16tdsg8 x1hl2dhg xggy1nq x1o1ewxj x3x9cwd x1e5q0jg x13rtm0m x87ps6o x1lku1pv x1a2a7pz x9f619 x3nfvp2 xdt5ytf xl56j7k x1n2onr6 xh8yej3");
var i = 0;
var addFriendCount = 0;

function addFriends () {
    if (list[i]) {
        if (list[i].getAttribute("aria-label") == "เพิ่มเป็นเพื่อน") {
            setTimeout(function () {
                list[i].click();
                addFriendCount = addFriendCount + 1;
                i = i + 1;
                console.log('เพิ่มเพื่อนสำเร็จคนที่ ' + addFriendCount);
                addFriends();
        }, 3000);
        } else {
            i = i + 1;
            addFriends();
        }
    } else {
        var scroll = document.getElementsByClassName("xb57i2i x1q594ok x5lxg6s x78zum5 xdt5ytf x6ikm8r x1ja2u2z x1pq812k x1rohswg xfk6m8 x1yqm8si xjx87ck xx8ngbg xwo3gff x1n2onr6 x1oyok0e x1odjw0f x1iyjqo2 xy5w88m");
        if (scroll) {
            console.log('แอดเพื่อนหมดแล้ว ทำการตรวจสอบใหม่');
            scroll[0].scrollTop = scroll[0].scrollHeight;
            setTimeout(function () {
                console.log('เริ่มการเพิ่มเพื่อนใหม่');
                scroll[0].scrollTop = 0;
                i = i + 1;
                addFriends();
            }, 3000);
        }
    }
}

addFriends();



