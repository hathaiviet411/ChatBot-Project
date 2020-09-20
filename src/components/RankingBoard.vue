<template>
    <div class="container-fluid dashboard">
        <div class="RankingBoard">
            <div class="row">

                <div class="col-lg col-sm">
                    <div class="card" id="qoutes">
                        <div class="card-body">
                            <div class="media align-items-center">
                                <div class="media-body">
                                    <span>"Wisdom is not a product from school, but a lifelong learning process." <br> "Trí tuệ không phải là một sản phẩm từ trường học, mà là một quá trình học tập suốt đời."</span>
                                </div>
                                <div class="text-center">
                                    <i class="icofont-education"></i>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="col-lg col-sm">
                    <div class="card" id="search">
                        <center>
                        <h4 id="title">Questions and Answers</h4>
                        <b-container class="bv-example-row">
                            <b-row>
                            <b-col class="col-8"><b-form-input v-model="keyword" type="text" debounce="500" placeholder="Search Question" id="keyword-input"></b-form-input></b-col>
                            <b-col class="col-4"><b-button>Search</b-button></b-col>
                            </b-row>
                        </b-container>
                        </center>
                    </div>
                </div>

            </div>
        </div>

        <div class="card question-list">
               
            <div class="container">
                <h3 class="text-center">Recommended Books To Improve Your Rank !</h3>
                <hr>
                <div class="wrapper">
                    <ul class="stage clearfix">

                        <li class="scene">
                            <div class="movie" onclick="return true">
                                <div class="poster"></div>
                                <div class="info">
                                    <header>
                                        <h1>It's a Wonderful Life</h1>
                                        <span class="year">1946</span>
                                        <span class="rating">PG</span>
                                        <span class="duration">130 minutes</span>
                                    </header>
                                    <p>
                                        In Bedford Falls, New York on Christmas Eve, George Bailey is deeply troubled. Prayers for his well-being from friends and family reach Heaven. Clarence Odbody, Angel Second Class, is assigned to visit Earth to save George, thereby earning his wings. Franklin and Joseph, the head angels, review George's life with Clarence.
                                    </p>
                                </div>
                            </div>
                        </li>

                        <li class="scene">
                            <div class="movie" onclick="return true">
                                <div class="poster"></div>
                                <div class="info">
                                    <header>
                                        <h1>Vengeance Valley</h1>
                                        <span class="year">1951</span>
                                        <span class="rating">NR</span>
                                        <span class="duration">83 minutes</span>
                                    </header>
                                    <p>
                                        A cattle baron takes in an orphaned boy and raises him, causing his own son to resent the boy. As they get older the resentment festers into hatred, and eventually the real son frames his stepbrother for fathering an illegitimate child that is actually his, seeing it as an opportunity to get his half-brother out of the way so he can have his father's empire all to himself.
                                    </p>
                                </div>
                            </div>
                        </li>

                        <li class="scene">
                            <div class="movie" onclick="return true">
                                <div class="poster"></div>
                                <div class="info">
                                    <header>
                                        <h1>The Gold Rush</h1>
                                        <span class="year">1925</span>
                                        <span class="rating">NR</span>
                                        <span class="duration">95 minutes</span>
                                    </header>
                                    <p>
                                        The Tramp travels to the Yukon to take part in the Klondike Gold Rush. He gets mixed up with some burly characters and falls in love with the beautiful Georgia. He tries to win her heart with his singular charm.
                                    </p>
                                </div>
                            </div>
                        </li>

                    </ul>
                    <p class="text-center">“When I look at a person, I see a person - not a rank, not a class, not a title.”
                        <br>
                        <span style="color: red"> ― Criss Jami, Killosophy</span>
                    </p>
                </div><!-- /wrapper -->
            </div><!-- /container -->
            <hr>

            <div class="title-card">
                <h4 class="text-center">Ranking Board</h4>
                <hr>
            </div>

            <div class="container imgRankList">
                <div class="row">
                    <div class="col-sm-5">
                        <img class="img-fluid" src="../assets/bronze.png" alt="Bronze">
                    </div>
                    <div class="col-sm-7">
                        <h6>Total Number: </h6> 
                        <h6>Top 5 Bronze Students: </h6>
                        <ul class="list-group">
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                        </ul>
                    </div>
                </div>
                <hr>
                <div class="row">
                    <div class="col-sm-5">
                        <img class="img-fluid" src="../assets/silver.png" alt="Silver">
                    </div>
                    <div class="col-sm-7">
                        <h6>Total Number: </h6> 
                        <h6>Top 5 Silver Students: </h6>
                        <ul class="list-group">
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                        </ul>
                    </div>
                </div>                
                <hr>
                <div class="row">
                    <div class="col-sm-5">
                        <img class="img-fluid" src="../assets/gold.png" alt="Gold">
                    </div>
                    <div class="col-sm-7">
                        <h6>Total Number: </h6> 
                        <h6>Top 5 Gold Students: </h6>
                        <ul class="list-group">
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                        </ul>
                    </div>
                </div>   
                <hr>
                <div class="row">
                    <div class="col-sm-5">
                        <img class="img-fluid" src="../assets/platinum.png" alt="Platinum">
                    </div>
                    <div class="col-sm-7">
                        <h6>Total Number: </h6> 
                        <h6>Top 5 Platinum Students: </h6>
                        <ul class="list-group">
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                        </ul>
                    </div>
                </div>
                <hr>
                <div class="row">
                    <div class="col-sm-5">
                        <img class="img-fluid" src="../assets/diamond.png" alt="Diamond">
                    </div>
                    <div class="col-sm-7">
                        <h6>Total Number: </h6> 
                        <h6>Top 5 Diamond Students: </h6>
                        <ul class="list-group">
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                        </ul>
                    </div>
                </div>    
                <hr>
                <div class="row">
                    <div class="col-sm-5">
                        <img class="img-fluid" src="../assets/master.png" alt="Master">
                    </div>
                    <div class="col-sm-7">
                        <h6>Total Number: </h6> 
                        <h6>Top 5 Master Students: </h6>
                        <ul class="list-group">
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                        </ul>
                    </div>
                </div>
                <hr>
                <div class="row">
                    <div class="col-sm-5">
                        <img class="img-fluid" src="../assets/gMaster.png" alt="gMaster">
                    </div>
                    <div class="col-sm-7">
                        <h6>Total Number: </h6> 
                        <h6>Top 5 Grand Master Students: </h6>
                        <ul class="list-group">
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                        </ul>
                    </div>
                </div>   
                <hr>
                <div class="row">
                    <div class="col-sm-5">
                        <img class="img-fluid" src="../assets/challenger.png" alt="Challenger">
                    </div>
                    <div class="col-sm-7">
                        <h6>Total Number: </h6> 
                        <h6>Top 5 Challenger Students: </h6>
                        <ul class="list-group">
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                            <li class="list-group-item">
                                <span class="badge">1st</span> -- Cras justo odio
                            </li>
                        </ul>
                    </div>
                </div>    
            </div> 
             <!--End Container Image  -->
        </div>
        <!-- End Card -->
    </div>
    <!-- End Main Container -->
</template>

<script>
// import axios from 'axios';
export default {
    name: 'RankingBoard',
}
</script>

<style scoped src="../assets/css/RankingBoard.css"></style>
<style scoped src="../assets/css/component.css"></style>
