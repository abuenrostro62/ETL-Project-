<body class="c3"><p class="c12"><span class="c6 c14">Project members: Araceli Buenrostro, Julie Mahoney, Michael Kuhn </span></p><p class="c11"><span class="c10"></span></p><p class="c11"><span class="c10"></span></p><p class="c12"><span class="c6 c5">What is the purpose of your data:</span></p><ul class="c0 lst-kix_vkpq7c5zk9cy-0 start"><li class="c1"><span class="c2">This dataset serve to answer questions such as:</span></li></ul><ul class="c0 lst-kix_vkpq7c5zk9cy-1 start"><li class="c4"><span class="c2">Is there a relationship between crime rates and housing prices by square foot?</span></li><li class="c4"><span class="c2">Is there a relationship between crime rates and grant applications?</span></li><li class="c4"><span class="c2">If so, which relationship is stronger?</span></li></ul><p class="c11"><span class="c2"></span></p><p class="c11"><span class="c2"></span></p><p class="c12"><span class="c6 c5">How will this database be used in the future?</span></p><ul class="c0 lst-kix_gt6qfwi79jk-0 start"><li class="c1"><span class="c2">Can be used to understand the best state(s) to move to when looking for safety, less expensive housing and/or number of grants applied to by school</span></li><li class="c1"><span class="c2">Relatively limited final database, given state-level information</span></li></ul><p class="c11"><span class="c2"></span></p><p class="c11"><span class="c2"></span></p><p class="c12"><span class="c5 c6">The databases</span></p><ul class="c0 lst-kix_uthfp532aeun-0 start"><li class="c1"><span class="c5">Housing (Zillow csv, compiled from Kaggle: </span><span class="c9 c5"><a class="c8" href="https://www.google.com/url?q=https://www.kaggle.com/zillow/zecon&amp;sa=D&amp;ust=1582409967950000">https://www.kaggle.com/zillow/zecon</a></span><span class="c2">)</span></li></ul><ul class="c0 lst-kix_uthfp532aeun-1 start"><li class="c4"><span class="c2">Price per sqft</span></li></ul><ul class="c0 lst-kix_uthfp532aeun-0"><li class="c1"><span class="c5">Crime (Kaggle csv, </span><span class="c5 c9"><a class="c8" href="https://www.google.com/url?q=https://www.kaggle.com/mikejohnsonjr/united-states-crime-rates-by-county/data&amp;sa=D&amp;ust=1582409967950000">https://www.kaggle.com/mikejohnsonjr/united-states-crime-rates-by-county/data</a></span><span class="c2">)</span></li></ul><ul class="c0 lst-kix_uthfp532aeun-1 start"><li class="c4"><span class="c5">Crime rate index by state/territory</span></li></ul><ul class="c0 lst-kix_uthfp532aeun-0"><li class="c1"><span class="c5">Education (</span><span class="c9 c5"><a class="c8" href="https://www.google.com/url?q=https://www.kaggle.com/theworldbank/education-statistics&amp;sa=D&amp;ust=1582409967951000">https://www.kaggle.com/theworldbank/education-statistics</a></span><span class="c2">, csv)</span></li></ul><ul class="c0 lst-kix_uthfp532aeun-1 start"><li class="c4"><span class="c2">2011 Grant Applicant Info:</span></li></ul><ul class="c0 lst-kix_uthfp532aeun-2 start"><li class="c12 c16"><span class="c2">Name of institution, city, state, application priority level &amp; institution type (Nonprofit, other). </span></li></ul><p class="c11"><span class="c2"></span></p><p class="c12"><span class="c6 c5">ETL Steps</span></p><ol class="c0 lst-kix_rwwqtpwq7peq-0 start" start="1"><li class="c1"><span class="c2">Identify and use worthy, reliable datasets</span></li></ol><p class="c11"><span class="c2"></span></p><p class="c7"><span class="c2">Datasets initially identified by county but then moved to state-level data to encompass all datasets</span></p><p class="c11"><span class="c2"></span></p><ol class="c0 lst-kix_rwwqtpwq7peq-0" start="2"><li class="c1"><span class="c2">Create and import tables into pgAdmin for cleaning</span></li></ol><p class="c7"><span class="c2">Adjust table names to ensure all data imports correctly</span></p><p class="c7 c13"><span class="c2"></span></p><ol class="c0 lst-kix_rwwqtpwq7peq-0" start="3"><li class="c1"><span class="c2">Clean databases via Postgres and Pandas</span></li></ol><p class="c11"><span class="c2"></span></p><p class="c12 c15"><span class="c2">Cleaning of data to ensure only needed columns are pulled</span></p><p class="c11 c15"><span class="c2"></span></p><p class="c7"><span class="c2">Concatenate fips state and county numbers to get fips numbers for data comparison (eventually not used)</span></p><p class="c11"><span class="c2"></span></p><ol class="c0 lst-kix_rwwqtpwq7peq-0" start="4"><li class="c1"><span class="c2">Join tables at a common element </span></li></ol><p class="c7 c13"><span class="c2"></span></p><p class="c7"><span class="c2">Join data based on fips state numbers to understand relationship between crime rate and housing prices per square foot data</span></p><p class="c11"><span class="c2"></span></p><p class="c7"><span class="c2">Join education data based on fips state number and state abbreviation to crime rate data</span></p><p class="c11"><span class="c2"></span></p><p class="c12"><span class="c6 c5">Major Challenges</span></p><ul class="c0 lst-kix_or47iehhyo4h-0 start"><li class="c1"><span class="c2">Finding datasets with enough overlap, with similar or fine granularity (county/state-level)</span></li><li class="c1"><span class="c2">Finding datasets that encompassed the same years</span></li><li class="c1"><span class="c2">Using pgAdmin throughout the process created a messy doc to follow&mdash;migrated content to Visual Studio to better organize and format</span></li><li class="c1"><span class="c2">Began with three very different data sets, so given the time to work, didn&rsquo;t have much time for relationship analysis at the end of the project </span></li></ul><p class="c11"><span class="c2"></span></p><p class="c12"><span class="c6 c5">Normalization</span></p><ul class="c0 lst-kix_c3gpd124spzx-0 start"><li class="c1"><span class="c2">Adjust all datasets to have a state fips number (one data set used state name, another used state abbreviations, etc)</span></li><li class="c1"><span class="c5">Rename columns so datasets could be joined and not have repeats </span></li></ul><p class="c11"><span class="c2"></span></p><p class="c11"><span class="c6 c5"></span></p></body>