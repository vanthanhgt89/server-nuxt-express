<template>
  <div class="container poster">
  <div class="row">
    <div class="col-sm-9 col-md-9">
      <div id="myCarousel" class="carousel slide" data-ride="carousel">
        <!-- Indicators -->
        <ol class="carousel-indicators">
          {% for item in poster %}
          {% if loop.index == 1 %}
          <li data-target="#myCarousel" data-slide-to="{{loop.index -1 }}" class="active"></li>
          {% else %}
          <li data-target="#myCarousel" data-slide-to="{{loop.index - 1}}"></li>
          {% endif %}
          {% endfor %}

        </ol>

        <!-- Wrapper for slides -->
        <div class="carousel-inner">
          {% for item in poster %} 
          {% if loop.index == 2 %}
          <div class="item active">
            <img src="/image/slider/{{item.url}}" style="width:100%;">
          </div>
          {% elif item.description == 'left' %}
           <div class="item">
            <img src="/image/slider/{{item.url}}" style="width:100%;">
          </div>
          {% else %}
          {% endif %} 
          {% endfor %}
        </div>
      </div>
    </div>

    <div class="col-sm-3 col-md-3 post">
      <img src="/image/quangcao/{{poster[0].url}}" alt="">
    </div>

  </div>
</div>
</template>
